---
title: funzione glPopClientAttrib (GL. h)
description: Le funzioni glPushClientAttrib e glPopClientAttrib salvano e ripristinano i gruppi di variabili di stato client nello stack dell'attributo client. | funzione glPopClientAttrib (GL. h)
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- funzione glPopClientAttrib OpenGL
topic_type:
- apiref
api_name:
- glPopClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9f09e9c7292754a736594a9bf3d57a70063744
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353351"
---
# <a name="glpopclientattrib-function"></a>glPopClientAttrib (funzione)

Le funzioni [**glPushClientAttrib**](glpushclientattrib.md) e **glPopClientAttrib** salvano e ripristinano i gruppi di variabili di stato client nello stack dell'attributo client.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                               | Significato                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_overflow dello stack GL \_**</dt> </dl> | La funzione è stata chiamata mentre lo stack dell'attributo client era pieno.<br/> |



## <a name="remarks"></a>Commenti

La funzione **glPushClientAttrib** usa il relativo parametro mask per determinare quali gruppi di variabili di stato client vengono salvati nello stack dell'attributo client. È possibile utilizzare l'operatore OR bit per bit per unire le costanti simboliche accettate per impostare bits e costruire una maschera.

La funzione **glPopClientAttrib** Ripristina i valori delle variabili di stato client salvate per ultime con **glPushclientAttrib**. Le variabili di stato client non salvate in precedenza rimangono invariate. Se si esegue il push degli attributi in uno stack di attributi client completo o se gli attributi vengono estratti da uno stack vuoto, viene impostato un flag di errore e non viene apportata alcuna modifica allo stato OpenGL. Per impostazione predefinita, lo stack dell'attributo client è vuoto.

Non è possibile salvare alcuni valori dello stato del client OpenGL nello stack dell'attributo client. Ad esempio, non è possibile salvare gli Stati SELECT o feedback nello stack dell'attributo client. La profondità dello stack dell'attributo client è almeno 16.

Le funzioni **glPushclientAttrib** e **glPopClientAttrib** non vengono compilate in elenchi di visualizzazione, ma vengono eseguite immediatamente.

Le funzioni **glPushClientAttrib** e **glPopClientAttrib** possono solo attivare le modalità di archiviazione in pixel e push e pop per gli Stati del client. È necessario usare [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) per eseguire il push e il pop degli stati conservati nel server.

> [!Note]  
> Le funzioni **glPushClientAttrib** e **glPopClientAttrib** sono disponibili solo in OpenGL versione 1,1 o successiva.

 

Le funzioni seguenti recuperano informazioni relative a **glPushClientAttrib** e **glPopClientAttrib**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ \_ profondità dello stack attrib del client GL \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ profondità massima \_ \_ \_ dello stack attrib \_ client

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
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

 

 





