# pymysql-connection-
#Integrating mysql with python
class db_connection:
    import pymysql

    def conn(self, host, user, password, db):
        conn = self.pymysql.connect(host, user, password, db).cursor()
        return conn


val = db_connection.conn(self=db_connection, host='localhost', user='root', password='1234', db='eie')


display_before_insert = 'select * from students'
query_insert = "insert into students values('8','achinthiya','ganesh','nci','22','da')"
dispaly_after_insert = 'select * from students'


val.execute(display_before_insert)
check = val.fetchall()
for row in check:
    print(row)

val.execute(query_insert)
val.execute(dispaly_after_insert)
print('##############################################################################')
check_1 = val.fetchall()
for rows in check_1:
    print(rows)

val.close()
