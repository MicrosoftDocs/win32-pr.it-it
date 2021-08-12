---
title: Funzione glGetColorTableParameterfvEXT (Gl.h)
description: Le funzioni glGetColorTableParameterfvEXT e glGetColorTableParameterivEXT ottengono i parametri della tavolozza dalle tabelle dei colori. | Funzione glGetColorTableParameterfvEXT (Gl.h)
ms.assetid: e78051aa-4233-413c-8838-0741b54eab0e
keywords:
- Funzione glGetColorTableParameterfvEXT OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterfvEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e7cd93c45c602b35e88fe28c467943829669d329f75007607783ece06f1b51b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118615771"
---
# <a name="glgetcolortableparameterfvext-function"></a>Funzione glGetColorTableParameterfvEXT

Le **funzioni glGetColorTableParameterfvEXT** e [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) ottengono i parametri della tavolozza dalle tabelle dei colori.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetColorTableParameterfvEXT(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Trama di destinazione della tavolozza per cui si desiderano i dati dei parametri. Deve essere TEXTURE \_ 1D, TEXTURE \_ 2D, PROXY \_ TEXTURE \_ 1D o PROXY \_ TEXTURE \_ 2D.

</dd> <dt>

*Pname* 
</dt> <dd>

Costante simbolica per il tipo di dati dei parametri del riquadro a cui *puntano i parametri*.

Di seguito sono riportate le costanti simboliche accettate e i relativi significati.



| Valore                                                                                                                                                                                                             | Significato                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ FORMAT \_ EXT**</dt> </dl>              | Restituisce il formato interno specificato dalla chiamata più recente a [**glColorTableEXT**](glcolortableext.md) o al valore predefinito.<br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ WIDTH \_ EXT**</dt> </dl>                 | Restituisce la larghezza della tavolozza corrente.<br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ RED \_ SIZE \_ EXT**</dt> </dl>       | Restituisce le dimensioni effettive usate internamente per archiviare il componente rosso dei dati del riquadro.<br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ GREEN \_ SIZE \_ EXT**</dt> </dl> | Restituisce le dimensioni effettive usate internamente per archiviare il componente verde dei dati del riquadro.<br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ BLUE \_ SIZE \_ EXT**</dt> </dl>    | Restituisce le dimensioni effettive usate internamente per archiviare il componente blu dei dati del riquadro.<br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <dt>**GL \_ COLOR \_ TABLE \_ ALPHA \_ SIZE \_ EXT**</dt> </dl> | Restituisce le dimensioni effettive usate internamente per archiviare il componente alfa dei dati del riquadro.<br/>                                         |



 

</dd> <dt>

*params* 
</dt> <dd>

Punta ai dati dei parametri della tabella dei colori specificati dal *parametro pname.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare le funzioni **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT** per recuperare dati specifici dei parametri dalle tabelle dei colori impostate con [**glColorTableEXT**](glcolortableext.md) per le tavolozze di trama di destinazione. È anche possibile usare queste funzioni per determinare il numero di voci della tabella dei colori restituite **da glGetColorTableEXT.**

Quando  il parametro di destinazione è GL PROXY TEXTURE 1D o GL PROXY TEXTURE 2D e l'implementazione non supporta i valori specificati per formato o \_ \_ \_ \_ \_ \_ *larghezza,* **glColorTableEXT**  può non riuscire a creare la tabella dei colori richiesta. In questo caso, la tabella dei colori è vuota e tutti i parametri recuperati saranno pari a zero. È possibile determinare se OpenGL supporta un formato e una dimensione di tabella a colori specifici chiamando **glColorTableEXT** con una destinazione proxy e quindi chiamando **glGetColorTableParameterivEXT** o **glGetColorTableParameterfvEXT** per determinare se il parametro width corrisponde a quello impostato da **glColorTableEXT**. Se la larghezza recuperata è zero, la richiesta di tabella colori da **parte di glColorTable non** è riuscita. Se la larghezza recuperata non è zero, è possibile chiamare **glColorTable** con la destinazione reale con TEXTURE 1D o TEXTURE 2D per impostare \_ \_ la tabella dei colori.

Le funzioni **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT** sono funzioni di estensione che non fanno parte della libreria OpenGL standard, ma fanno parte dell'estensione della trama con tavolozza GL \_ \_ EXT. \_ Per verificare se l'implementazione di OpenGL supporta **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT,** chiamare [**glGetString**](glgetstring.md)**(** GL \_ EXTENSIONS **).** Se restituisce una trama con tavolozza GL \_ EXT, sono supportati \_ \_ **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT.** Per ottenere l'indirizzo della funzione di una funzione di estensione, chiamare [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





