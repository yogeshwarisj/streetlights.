from flask import Flask, request, jsonify

app=Flask(__name__)

streetlight_list=[
    {
    'id':1,
    'area_name': 'Silvanagar',
    'color': 'Yellow',
    'sensorpin': 'A0',
    'sensorvalue': 'Bellow 100',
    'state': 'On',
    'delay': '1000',
    },
    {
    'id':2,
    'area_name': 'Virajpet',
    'color': 'White',
    'sensorpin': 'A0',
    'sensorvalue': 'Above 100',
    'state': 'Off',
    'delay': 'Sensorvalue',
    },
    {
    'id':3,
    'area_name': 'Vinayakanagar',
    'color': 'Red',
    'sensorpin': 'A0',
    'sensorvalue': 'Bellow 100',
    'state': 'On',
    'delay': '1000',
    },
    {
    'id':4,
    'area_name': 'Vidyanagar',
    'color': 'Blue',
    'sensorpin': 'A0',
    'sensorvalue': 'Above 100',
    'state': 'Off',
    'delay': 'Sensorvalue',
    }
    ]
    
    
    @app.route('/streetlight',methods=['GET','POST'])
    def streetlight():
        if request.method == 'GET':
            if len(streetlight_list)<1:
                return 'cannot detect',+'404'
            else:
                return jsonify(streetlight_list)
        if request.method == 'POST':
            new_area=request.form['area']
            new_color=request.form['color']
            new_sensorpin=request.form['sensorpin']
            new_sensorvalue=request.form['sensorvalue']
            new_state.request.form['state']
            iD=streetlight_list[-1]['id']+1
            
            new_obj={
                'id':iD,
                'area_name':new_area,
                'color':new_color,
                'sensorpin':new_sensorpin,
                'sensorvalue':new_sensorvalue,
                'state':new_state,
            }
            streetlight_list.append(new_obj)
            return jsonify(streetlight_list)
            
    if __name__ == '__main__':
        app.run(debug=True)
