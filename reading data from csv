def parse_headers(header_line):         # for headers
  return header_line.strip().split()

def parse_values(data_line):            # for values
  values=[]
  for item in data_line.strip().split(','):
    if item == '':
      values.append(0.0)
    else:
      values.append(float(item))
  return values


def create_item_dict(values,header):

  result={} #result is dictionary 

  for values,header in zip(values,headers):  # 
    result[header]=values  #header attribute ko konsi value deni hai a:1 hi hoga

  return result 


def read_csv(path):
  result=[]

  #open file in read mode 
  with open(path,'r') as f:
    lines = f.readlines()  #gives the lines line by line 

    headers = parse_headers(lines[0])

    for data_line in lines[1:]:

      values = parse_values(data_line)

      item_dict = create_item_dict(values,headers)

      result.append(item_dict)
  return result
