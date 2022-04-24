# pickle-or-json-


def serialize(obj,file,type) :
    if type== 'pickle':
        import pickle
        with open(file,'wb') as f:
            pickle.dump(obj,f)
    elif type== 'json' :
        import json
        with open(file,'w')  as f:
            json.dump(obj,f)
    else:
        print('Invalid Serlization.Use Pickle or Json')



        def deserialize (file,type):
            if type == 'pickle' :
                import pickle
                with open(file, 'rb') as f :
                    obj= pickle.load(f)
                    return obj
            elif type== 'json' :
                import json
                with open(file, 'r') as f:
                    obj=json.load(f)
                    return obj
            else:
                print('Invalid Serialization,Use pickle or json!')

                
