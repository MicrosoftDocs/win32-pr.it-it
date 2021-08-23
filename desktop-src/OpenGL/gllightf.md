---
title: Funzione glLightf (Gl.h)
description: La funzione glLightf restituisce i valori del parametro light source.
ms.assetid: d9f93fd9-6674-486f-a3fc-c10255dd37e7
keywords:
- Funzione glLightf OpenGL
topic_type:
- apiref
api_name:
- glLightf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde2bbee996183ad39067aed3b98a64dd5abb40f87c6746d7dda305bdb0e7438
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012109"
---
# <a name="gllightf-function"></a>Funzione glLightf

La **funzione glLightf** restituisce i valori del parametro light source.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLightf(
   GLenum  light,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*light* 
</dt> <dd>

Identificatore di una luce. Il numero di luci possibili dipende dall'implementazione, ma sono supportate almeno otto luci. Sono identificati da nomi simbolici nel formato GL LIGHT i dove i è \_ un valore: da 0 a GL MAX LIGHTS -  \_ \_ 1.

</dd> <dt>

*Pname* 
</dt> <dd>

Parametro di sorgente di luce a valore singolo per *la luce*. Vengono accettati i nomi simbolici seguenti.



| Valore                                                                                                                                                                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**GL \_ SPOT \_ EXPONENT**</dt> </dl>                                                                                                                                                                             | Il *parametro param* è un singolo valore a virgola mobile che specifica la distribuzione dell'intensità della luce. I valori a virgola mobile vengono mappati direttamente. Vengono accettati solo i \[ valori nell'intervallo 0, 128. \] <br/> L'intensità della luce effettiva viene attenuata dal coseno dell'angolo tra la direzione della luce e la direzione dalla luce al vertice che viene illuminato, elevato alla potenza dell'esponente spot. Di conseguenza, gli esponenti spot più elevati hanno come risultato una sorgente di luce più mirata, indipendentemente dall'angolo di taglio del punto. L'esponente spot predefinito è 0, con conseguente distribuzione uniforme della luce.<br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL \_ SPOT \_ CUTOFF**</dt> </dl>                                                                                                                                                                                   | Il *parametro param* è un singolo valore a virgola mobile che specifica l'angolo di distribuzione massimo di una sorgente di luce. I valori a virgola mobile vengono mappati direttamente. Vengono accettati solo i \[ valori nell'intervallo 0, 90 e il valore \] speciale 180. <br/> Se l'angolo tra la direzione della luce e la direzione dalla luce al vertice da allaggerire è maggiore dell'angolo di taglio spot, la luce è completamente mascherata. In caso contrario, l'intensità è controllata dall'esponente spot e dai fattori di attenuazione. Il valore predefinito di cutoff spot è 180, con conseguente distribuzione uniforme della luce.<br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**ATTENUAZIONE \_ \_ COSTANTE GL, \_ \_ ATTENUAZIONE LINEARE GL, \_ ATTENUAZIONE QUADRATICA GL \_**</dt> </dl> | Il *parametro param* è un singolo valore a virgola mobile che specifica uno dei tre fattori di attenuazione della luce. I valori a virgola mobile vengono mappati direttamente. Vengono accettati solo valori non negativi. <br/> Se la luce è posizionale, anziché direzionale, la sua intensità viene attenuata dal reciproco della somma di: il fattore costante, il fattore lineare moltiplicato per la distanza tra la luce e il vertice da allaggerire e il fattore quadratico moltiplicato per il quadrato della stessa distanza. I fattori di attenuazione predefiniti sono (1,0,0) e non determinano alcuna attenuazione.<br/>                   |



 

</dd> <dt>

*param* 
</dt> <dd>

Specifica il valore su cui verrà impostato *il parametro pname* della *luce* sorgente di luce.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *light* o *pname* non è un valore accettato.<br/>                                                                                                                                                                  |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | È stato specificato un valore dell'esponente spot non compreso nell'intervallo 0, 128 o un valore di taglio spot non compreso nell'intervallo 0, 90 (ad eccezione del valore speciale \[ \] \[ 180) oppure è stato specificato un fattore di \] attenuazione negativo.<br/> |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                                                     |



## <a name="remarks"></a>Commenti

La **funzione glLightf** imposta il valore o i valori dei singoli parametri della sorgente di luce. Il *parametro light* denota la luce ed è un nome simbolico nel formato GL LIGHT i , dove \_ 0 = i *<* GL MAX \_ \_ LIGHTS.

Il *parametro pname* specifica uno dei parametri light source, anche in questo caso in base al nome simbolico. Il *parametro param* è un singolo valore o un puntatore a una matrice che contiene i nuovi valori.

Il calcolo dell'illuminazione è abilitato e disabilitato [**usando glEnable**](glenable.md) [**e glDisable con**](gldisable.md) l'argomento GL \_ LIGHTING. Quando l'illuminazione è abilitata, le sorgenti di luce abilitate contribuiscono al calcolo dell'illuminazione. La *sorgente di luce i* è abilitata e disabilitata usando **glEnable** **e glDisable con** l'argomento GL LIGHT \_ *i*.

È sempre il caso in cui GL \_ LIGHT *i* = GL \_ LIGHT0 + *i*.

Le funzioni seguenti recuperano informazioni correlate alla **funzione glLightf:**

[**glGetLight**](glgetlight.md)

[**glIsEnabled con**](glisenabled.md) argomento GL \_ LIGHTING

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





