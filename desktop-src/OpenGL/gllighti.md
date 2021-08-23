---
title: Funzione glLighti (Gl.h)
description: La funzione glLighti restituisce i valori dei parametri di origine chiaro.
ms.assetid: 4fa5e604-d45d-412e-a08c-c38e0836596f
keywords:
- Funzione glLighti OpenGL
topic_type:
- apiref
api_name:
- glLighti
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94ec260f0e4e5475cc834c786bc1ba7249b30fabd087030caf3426273adc3012
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493311"
---
# <a name="gllighti-function"></a>Funzione glLighti

La **funzione glLighti** restituisce i valori dei parametri di origine chiaro.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLighti(
   GLenum light,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*light* 
</dt> <dd>

Identificatore di una luce. Il numero di possibili luci dipende dall'implementazione, ma sono supportate almeno otto luci. Sono identificati da nomi simbolici nel formato GL \_ LIGHT *i* dove *i* è un valore: da 0 a GL \_ MAX LIGHTS - \_ 1.

</dd> <dt>

*Pname* 
</dt> <dd>

Parametro di origine di luce a valore singolo per *light*. Vengono accettati i nomi simbolici seguenti.



| Valore                                                                                                                                                                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**ESPONENTE DI GL \_ SPOT \_**</dt> </dl>                                                                                                                                                                             | Il *parametro param* è un singolo valore integer che specifica la distribuzione dell'intensità della luce. I valori interi e a virgola mobile vengono mappati direttamente. Vengono accettati solo i \[ valori nell'intervallo 0, 128. \] <br/> L'intensità effettiva della luce viene attenuata dal coseno dell'angolo tra la direzione della luce e la direzione dalla luce al vertice da illuminare, alzata alla potenza dell'esponente spot. Di conseguenza, gli esponenti spot più alti comportano una sorgente di luce più mirata, indipendentemente dall'angolo di taglio della spot. L'esponente spot predefinito è 0, con conseguente distribuzione uniforme della luce.<br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL \_ SPOT \_ CUTOFF**</dt> </dl>                                                                                                                                                                                   | Il *parametro param* è un singolo valore integer che specifica l'angolo massimo di diffusione di una sorgente di luce. I valori interi e a virgola mobile vengono mappati direttamente. Vengono accettati solo i \[ valori nell'intervallo 0, 90 e \] il valore speciale 180. <br/> Se l'angolo tra la direzione della luce e la direzione dalla luce al vertice da illuminare è maggiore dell'angolo di taglio spot, la luce viene completamente mascherata. In caso contrario, l'intensità è controllata dall'esponente spot e dai fattori di attenuazione. Il cutoff spot predefinito è 180, con conseguente distribuzione uniforme della luce.<br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**ATTENUAZIONE \_ \_ COSTANTE GL, \_ \_ ATTENUAZIONE LINEARE GL, \_ ATTENUAZIONE \_ QUADRATICA GL**</dt> </dl> | Il *parametro param* è un singolo valore integer che specifica uno dei tre fattori di attenuazione della luce. I valori interi e a virgola mobile vengono mappati direttamente. Vengono accettati solo valori non negativi. <br/> Se la luce è posizionale, anziché direzionale, l'intensità viene attenuata dal reciproco della somma di: il fattore costante, il fattore lineare moltiplicato per la distanza tra la luce e il vertice da illuminare e il fattore quadratico moltiplicato per il quadrato della stessa distanza. I fattori di attenuazione predefiniti sono (1,0,0) e non determinano alcuna attenuazione.<br/>                   |



 

</dd> <dt>

*param* 
</dt> <dd>

Specifica il valore su cui verrà impostato *il parametro pname* della luce *sorgente* di luce.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *light* o *pname* non è un valore accettato.<br/>                                                                                                                                                                  |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | È stato specificato un valore esponente spot non compreso nell'intervallo 0, 128 o cutoff spot non compreso nell'intervallo 0, 90 (ad eccezione del valore speciale \[ \] \[ 180) o è stato specificato un fattore di \] attenuazione negativo.<br/> |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                                                     |



## <a name="remarks"></a>Commenti

La **funzione glLighti** imposta il valore o i valori dei singoli parametri della sorgente di luce. Il *parametro light* denota la luce e è un nome simbolico nel formato GL LIGHT i , dove 0 = i < GL MAX \_   \_ \_ LIGHTS.

Il *parametro pname* specifica uno dei parametri della sorgente di luce, sempre in base al nome simbolico. Il *parametro param* è un singolo valore o un puntatore a una matrice che contiene i nuovi valori.

Il calcolo dell'illuminazione è abilitato e disabilitato [**usando glEnable**](glenable.md) [**e glDisable con**](gldisable.md) l'argomento GL \_ LIGHTING. Quando l'illuminazione è abilitata, le sorgenti di luce abilitate contribuiscono al calcolo dell'illuminazione. La *sorgente di* luce i è abilitata e disabilitata usando **glEnable** **e glDisable con** l'argomento GL LIGHT \_ *i*.

È sempre il caso che GL \_ LIGHT *i* = GL \_ LIGHT0 + *i*.

Le funzioni seguenti recuperano informazioni correlate alla **funzione glLighti:**

[**glGetLight**](glgetlight.md)

[**glIsEnabled con**](glisenabled.md) l'argomento GL \_ LIGHTING

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

 

 





