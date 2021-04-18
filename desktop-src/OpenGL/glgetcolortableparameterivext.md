---
title: funzione glGetColorTableParameterivEXT (GL. h)
description: Le funzioni glGetColorTableParameterfvEXT e glGetColorTableParameterivEXT ottengono i parametri della tavolozza dalle tabelle dei colori. | funzione glGetColorTableParameterivEXT (GL. h)
ms.assetid: 39a0b346-d103-4426-8536-95e7e1548f7a
keywords:
- funzione glGetColorTableParameterivEXT OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterivEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897dd11781968838bb8c26a716e3857acc119e9c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321798"
---
# <a name="glgetcolortableparameterivext-function"></a>glGetColorTableParameterivEXT (funzione)

Le funzioni [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) e **glGetColorTableParameterivEXT** ottengono i parametri della tavolozza dalle tabelle dei colori.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetColorTableParameterivEXT(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Trama di destinazione della tavolozza per cui si desiderano i dati dei parametri. Deve essere una trama \_ 1D, una trama \_ 2D, una \_ trama proxy \_ 1D o una trama del proxy \_ \_ 2D.

</dd> <dt>

*pname* 
</dt> <dd>

Costante simbolica per il *tipo di dati* del parametro della tavolozza a cui puntano i parametri.

Di seguito sono riportate le costanti simboliche accettate e i relativi significati.



| Valore                                                                                                                                                                                                             | Significato                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <dt>**\_ \_ formato tabella colori \_ GL \_ ext**</dt> </dl>              | Restituisce il formato interno specificato dalla chiamata più recente a [**glColorTableEXT**](glcolortableext.md) o il valore predefinito.<br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <dt>**\_ \_ Larghezza tabella colori \_ GL \_ ext**</dt> </dl>                 | Restituisce la larghezza della tavolozza corrente.<br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <dt>**\_ \_ \_ dimensioni rosse tabella colori \_ GL \_ ext**</dt> </dl>       | Restituisce la dimensione effettiva utilizzata internamente per archiviare il componente rosso dei dati della tavolozza.<br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <dt>**\_ \_ \_ dimensioni verdi tabella colore \_ GL \_ ext**</dt> </dl> | Restituisce la dimensione effettiva utilizzata internamente per archiviare il componente verde dei dati della tavolozza.<br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <dt>**\_ \_ \_ dimensioni blu tabella colori \_ GL \_ ext**</dt> </dl>    | Restituisce la dimensione effettiva utilizzata internamente per archiviare il componente blu dei dati della tavolozza.<br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <dt>**\_ \_ \_ dimensioni alfa tabella colori \_ GL \_ ext**</dt> </dl> | Restituisce la dimensione effettiva utilizzata internamente per archiviare il componente alfa dei dati della tavolozza.<br/>                                         |



 

</dd> <dt>

*params* 
</dt> <dd>

Punta ai dati dei parametri della tabella dei colori specificati dal parametro *pname* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare le funzioni **glGetColorTableParameterivEXT** e [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) per recuperare dati di parametri specifici dalle tabelle dei colori impostate con [**glColorTableEXT**](glcolortableext.md) per le tavolozze delle trame di destinazione. È anche possibile usare queste funzioni per determinare il numero di voci della tabella dei colori restituite da **glGetColorTableEXT** .

Quando il parametro di *destinazione* è GL \_ proxy \_ texture \_ 1D o \_ GL proxy \_ texture \_ 2D e l'implementazione non supporta i valori specificati per il *formato* o la *larghezza*, **glColorTableEXT** può non essere in grado di creare la tabella dei colori richiesta. In questo caso, la tabella dei colori è vuota e tutti i parametri recuperati saranno pari a zero. È possibile determinare se OpenGL supporta un formato e una dimensione della tabella dei colori specifici chiamando **glColorTableEXT** con una destinazione proxy e quindi chiamando **glGetColorTableParameterivEXT** o [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) per determinare se il parametro width corrisponde a quello impostato da **glColorTableEXT**. Se la larghezza recuperata è zero, la richiesta della tabella dei colori di **glColorTable** non è riuscita. Se la larghezza recuperata è diversa da zero, è possibile chiamare **glColorTable** con la destinazione reale con trama \_ 1D o trama \_ 2D per impostare la tabella dei colori.

Le funzioni **glGetColorTableParameterivEXT** e [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) sono funzioni di estensione che non fanno parte della libreria OpenGL standard, ma che fanno parte dell' \_ estensione di trama GL ext \_ tavolozza \_ . Per verificare se l'implementazione di OpenGL supporta **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT**, chiamare [**glGetString**](glgetstring.md)**(** GL \_ Extensions **)**. Se restituisce la \_ trama della \_ tavolozza GL ext \_ , **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT** sono supportati. Per ottenere l'indirizzo della funzione di una funzione di estensione, chiamare [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





