---
title: Funzione glLightiv (Gl.h)
description: La funzione glLightiv restituisce i valori dei parametri di origine chiaro.
ms.assetid: 927f6a7e-be42-46ab-9c23-6ce87f96bd8a
keywords:
- Funzione glLightiv OpenGL
topic_type:
- apiref
api_name:
- glLightiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b497c6cbac510b57814303f07ee060398e255b02dd1c8f9d7cd129f386d776
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493251"
---
# <a name="gllightiv-function"></a>Funzione glLightiv

La **funzione glLightiv** restituisce i valori dei parametri di origine chiaro.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLightiv(
         GLenum light,
         GLenum pname,
   const GLint  *params
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

Parametro della sorgente di luce per *light*. Vengono accettati i nomi simbolici seguenti.



| Valore                                                                                                                                                                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**AMBIENTE \_ GL**</dt> </dl>                                                                                                                                                                                                | Il *parametro params* contiene quattro valori interi che specificano l'intensità RGBA ambientale della luce. I valori interi vengono mappati in modo lineare in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo sia mappato a -1,0. I valori a virgola mobile vengono mappati direttamente. Né i valori integer né i valori a virgola mobile sono a virgola mobile. L'intensità della luce ambientale predefinita è (0,0, 0,0, 0,0, 1,0). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFFUSE**</dt> </dl>                                                                                                                                                                                                | Il *parametro params* contiene quattro valori interi che specificano l'intensità RGBA diffusa della luce. I valori interi vengono mappati in modo lineare in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo sia mappato a -1,0. I valori a virgola mobile vengono mappati direttamente. Né i valori integer né i valori a virgola mobile sono a virgola mobile. L'intensità diffusa predefinita è (0,0, 0,0, 0,0, 1,0) per tutte le luci diverse da zero chiaro. L'intensità diffusa predefinita di zero chiaro è (1,0, 1,0, 1,0, 1,0). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_SPECULARE GL**</dt> </dl>                                                                                                                                                                                             | Il *parametro params* contiene quattro valori interi che specificano l'intensità RGBA speculare della luce. I valori interi vengono mappati in modo lineare in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo a 1,0. I valori a virgola mobile vengono mappati direttamente. Né i valori integer né i valori a virgola mobile sono a virgola mobile. L'intensità speculare predefinita è (0,0, 0,0, 0,0, 1,0) per tutte le luci diverse da zero chiaro. L'intensità speculare predefinita di zero chiaro è (1,0, 1,0, 1,0, 1,0).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**POSIZIONE \_ DI CONTABILITÀ GENERALE**</dt> </dl>                                                                                                                                                                                             | Il *parametro params* contiene quattro valori interi che specificano la posizione della luce nelle coordinate dell'oggetto omogenee. Viene eseguito direttamente il mapping di valori interi e a virgola mobile. Né i valori integer né i valori a virgola mobile sono a virgola mobile. <br/> La posizione viene trasformata dalla matrice modelview quando viene chiamato [**glLightiv**](gllightfv.md) (proprio come se fosse un punto) e viene archiviata in coordinate oculare. Se il *componente w* della posizione è 0,0, la luce viene considerata come una sorgente direzionale. I calcoli di illuminazione diffusa e speculare prendono in considerazione la direzione della luce, ma non la posizione effettiva, e l'attenuazione è disabilitata. In caso contrario, i calcoli di illuminazione diffusa e speculare si basano sulla posizione effettiva della luce nelle coordinate oculari e l'attenuazione è abilitata. La posizione predefinita è (0,0,1,0); Di conseguenza, la sorgente di luce predefinita è direzionale, parallela a e nella direzione dell'asse -*z.*<br/> |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**DIREZIONE \_ DEL PUNTO \_ GL**</dt> </dl>                                                                                                                                                                          | Il *parametro params* contiene tre valori interi che specificano la direzione della luce nelle coordinate dell'oggetto omogenee. Viene eseguito direttamente il mapping di valori interi e a virgola mobile. Né i valori integer né i valori a virgola mobile sono a virgola mobile. <br/> La direzione del punto viene trasformata dall'inverso della matrice modelview quando viene chiamato **glLightiv** (proprio come se fosse una normale) e viene archiviata nelle coordinate oculare. È significativo solo quando GL \_ SPOT \_ CUTOFF non è 180, ovvero per impostazione predefinita. La direzione predefinita è (0,0,1).<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**ESPONENTE DI GL \_ SPOT \_**</dt> </dl>                                                                                                                                                                             | Il *parametro params* è un singolo valore integer che specifica la distribuzione dell'intensità della luce. I valori interi e a virgola mobile vengono mappati direttamente. Vengono accettati solo i \[ valori nell'intervallo 0, 128. \] <br/> L'intensità effettiva della luce viene attenuata dal coseno dell'angolo tra la direzione della luce e la direzione dalla luce al vertice da illuminare, alzata alla potenza dell'esponente spot. Di conseguenza, gli esponenti spot più alti comportano una sorgente di luce più mirata, indipendentemente dall'angolo di taglio della spot. L'esponente spot predefinito è 0, con conseguente distribuzione uniforme della luce.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL \_ SPOT \_ CUTOFF**</dt> </dl>                                                                                                                                                                                   | Il *parametro params* è un singolo valore integer che specifica l'angolo massimo di diffusione di una sorgente di luce. I valori interi e a virgola mobile vengono mappati direttamente. Vengono accettati solo i \[ valori nell'intervallo 0, 90 e \] il valore speciale 180. <br/> Se l'angolo tra la direzione della luce e la direzione dalla luce al vertice da illuminare è maggiore dell'angolo di taglio spot, la luce viene completamente mascherata. In caso contrario, l'intensità è controllata dall'esponente spot e dai fattori di attenuazione. Il cutoff spot predefinito è 180, con conseguente distribuzione uniforme della luce.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**ATTENUAZIONE \_ \_ COSTANTE GL, \_ \_ ATTENUAZIONE LINEARE GL, \_ ATTENUAZIONE \_ QUADRATICA GL**</dt> </dl> | Il *parametro params* è un singolo valore integer che specifica uno dei tre fattori di attenuazione della luce. I valori interi e a virgola mobile vengono mappati direttamente. Vengono accettati solo valori non negativi. <br/> Se la luce è posizionale, anziché direzionale, l'intensità viene attenuata dal reciproco della somma di: il fattore costante, il fattore lineare moltiplicato per la distanza tra la luce e il vertice da illuminare e il fattore quadratico moltiplicato per il quadrato della stessa distanza. I fattori di attenuazione predefiniti sono (1,0,0) e non determinano alcuna attenuazione.<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*params* 
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

La **funzione glLightiv** imposta il valore o i valori dei singoli parametri della sorgente di luce. Il *parametro light* denota la luce e è un nome simbolico nel formato GL LIGHT i , dove 0 = i < GL MAX \_   \_ \_ LIGHTS.

Il *parametro pname* specifica uno dei parametri della sorgente di luce, sempre in base al nome simbolico. Il *parametro params* è un singolo valore o un puntatore a una matrice che contiene i nuovi valori.

Il calcolo dell'illuminazione è abilitato e disabilitato [**usando glEnable**](glenable.md) [**e glDisable con**](gldisable.md) l'argomento GL \_ LIGHTING. Quando l'illuminazione è abilitata, le sorgenti di luce abilitate contribuiscono al calcolo dell'illuminazione. La *sorgente di* luce i è abilitata e disabilitata usando **glEnable** **e glDisable con** l'argomento GL LIGHT \_ *i*.

È sempre il caso che GL \_ LIGHT *i* = GL \_ LIGHT0 + *i*.

Le funzioni seguenti recuperano informazioni correlate alla **funzione glLightiv:**

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

 

 





