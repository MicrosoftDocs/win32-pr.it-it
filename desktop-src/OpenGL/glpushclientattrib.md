---
title: Funzione glPushClientAttrib (Gl.h)
description: Le funzioni glPushClientAttrib e glPopClientAttrib salvano e ripristinano gruppi di variabili di stato client nello stack degli attributi client. | Funzione glPushClientAttrib (Gl.h)
ms.assetid: 69f28af6-1023-4546-95ff-169525c23b07
keywords:
- Funzione glPushClientAttrib OpenGL
topic_type:
- apiref
api_name:
- glPushClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f378ec3ff735ed916567ea91e211a1d8a1685580b1f1ea80d448b92203b39a3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492611"
---
# <a name="glpushclientattrib-function"></a>Funzione glPushClientAttrib

Le **funzioni glPushClientAttrib** e [**glPopClientAttrib**](glpopclientattrib.md) salvano e ripristinano gruppi di variabili di stato client nello stack di attributi client.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPushClientAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Maschera* 
</dt> <dd>

Maschera che indica gli attributi da salvare. Di seguito sono riportate le costanti della maschera simbolica e i relativi stati client OpenGL associati.



| Valore                                                                                                                                                                                                                                            | Significato                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_CLIENT_PIXEL_STORE_BIT"></span><span id="gl_client_pixel_store_bit"></span><dl> <dt>**BIT \_ \_ DELL'ARCHIVIO PIXEL \_ DEL \_ CLIENT GL**</dt> </dl>                                             | Attributi della modalità di archiviazione pixel.<br/>         |
| <span id="GL_CLIENT_VERTEX_ARRAY_BIT"></span><span id="gl_client_vertex_array_bit"></span><dl> <dt>**BIT \_ DI MATRICE DEI VERTICI CLIENT GL \_ \_ \_**</dt> </dl>                                          | Attributi della matrice di vertici.<br/>               |
| <span id="GL_CLIENT_ALL_ATTRIB_BITs"></span><span id="gl_client_all_attrib_bits"></span><span id="GL_CLIENT_ALL_ATTRIB_BITS"></span><dl> <dt>**GL \_ CLIENT \_ ALL \_ ATTRIB \_ BITs**</dt> </dl> | tutti gli attributi dello stato client impilabili.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                               | Significato                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**OVERFLOW DELLO STACK GL \_ \_**</dt> </dl> | La funzione è stata chiamata mentre lo stack dell'attributo client era pieno.<br/> |



## <a name="remarks"></a>Commenti

La **funzione glPushClientAttrib** usa il parametro mask per determinare quali gruppi di variabili di stato client vengono salvati nello stack degli attributi client. È possibile usare l'operatore OR bit per bit per unire le costanti simboliche accettate per impostare bit e costruire una maschera.

La [**funzione glPopClientAttrib**](glpopclientattrib.md) ripristina i valori delle variabili di stato client salvate per l'ultima volta con **glPushclientAttrib**. Le variabili di stato client non salvate in precedenza rimangono invariate. Il push degli attributi in uno stack completo di attributi client o la rimozione di attributi da uno stack vuoto imposta un flag di errore e non vengono apportate altre modifiche allo stato OpenGL. Per impostazione predefinita, lo stack di attributi client è vuoto.

Alcuni valori di stato client OpenGL non possono essere salvati nello stack di attributi client. Ad esempio, non è possibile salvare gli stati di selezione o feedback nello stack di attributi client. La profondità dello stack di attributi client è almeno 16.

Le **funzioni glPushclientAttrib** e **glPopClientAttrib** non vengono compilate in elenchi di visualizzazione, ma vengono eseguite immediatamente.

Le **funzioni glPushClientAttrib** e **glPopClientAttrib** possono solo eseguire push e pop delle modalità di archiviazione pixel e degli stati client dell'array di vertici. È necessario usare [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) per eseguire il push e il pop degli stati mantenuti nel server.

> [!Note]  
> Le **funzioni glPushClientAttrib** e **glPopClientAttrib** sono disponibili solo in OpenGL versione 1.1 o successiva.

 

Le funzioni seguenti recuperano informazioni correlate **a glPushClientAttrib** e **glPopClientAttrib**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ CLIENT \_ ATTRIB STACK \_ \_ DEPTH

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MAX CLIENT \_ \_ ATTRIB STACK \_ \_ DEPTH

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDisableClientState**](gldisableclientstate.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





