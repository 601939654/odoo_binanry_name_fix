# odoo_binanry_name_fix
odoo binary字段，文件名错误问题处理


一般都需要定义一个文件名字段，如下：

multimedia = fields.Binary(string='多媒体', required=True)

multimedia_name = fields.Char(string="多媒体名称")



另外再xml中要定义出这个字段，将文件名字段隐藏即可，如下：

<field name="multimedia_name" invisible="1"/>

<field name="multimedia" filename="multimedia_name"/>

