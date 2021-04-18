---
title: funzione glLightiv (GL. h)
description: La funzione glLightiv restituisce i valori dei parametri di origine chiaro.
ms.assetid: 927f6a7e-be42-46ab-9c23-6ce87f96bd8a
keywords:
- funzione glLightiv OpenGL
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
ms.openlocfilehash: 8c70e991cf96ed5d3565e1b6c9522693786cca80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301007"
---
# <a name="gllightiv-function"></a>glLightiv (funzione)

La funzione **glLightiv** restituisce i valori dei parametri di origine chiaro.

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

Identificatore di una luce. Il numero di spie possibili dipende dall'implementazione, ma sono supportate almeno otto luci. Sono identificati da nomi simbolici nel formato GL \_ Light *i* dove *i* è un valore: da 0 a GL \_ Max \_ Lights-1.

</dd> <dt>

*pname* 
</dt> <dd>

Parametro della sorgente di luce per la *luce*. I nomi simbolici seguenti sono accettati.



| Valore                                                                                                                                                                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**\_ambiente GL**</dt> </dl>                                                                                                                                                                                                | Il parametro *params* contiene quattro valori integer che specificano l'intensità RGBA di ambiente della luce. Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0. Ai valori a virgola mobile viene eseguito il mapping diretto. Non vengono bloccati né i valori integer né i valori a virgola mobile. L'intensità di luce di ambiente predefinita è (0,0, 0,0, 0,0, 1,0). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ diffuse**</dt> </dl>                                                                                                                                                                                                | Il parametro *params* contiene quattro valori integer che specificano l'intensità RGBA diffusa della luce. Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0. Ai valori a virgola mobile viene eseguito il mapping diretto. Non vengono bloccati né i valori integer né i valori a virgola mobile. L'intensità diffusa predefinita è (0,0, 0,0, 0,0, 1,0) per tutte le luci diverse dallo zero chiaro. L'intensità diffusa predefinita dello zero chiaro è (1,0, 1,0, 1,0, 1,0). <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_speculare GL**</dt> </dl>                                                                                                                                                                                             | Il parametro *params* contiene quattro valori integer che specificano l'intensità RGBA speculare della luce. Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a 1,0. Ai valori a virgola mobile viene eseguito il mapping diretto. Non vengono bloccati né i valori integer né i valori a virgola mobile. L'intensità speculare predefinita è (0,0, 0,0, 0,0, 1,0) per tutte le luci diverse dallo zero chiaro. L'intensità speculare predefinita dello zero chiaro è (1,0, 1,0, 1,0, 1,0).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**\_posizione GL**</dt> </dl>                                                                                                                                                                                             | Il parametro *params* contiene quattro valori integer che specificano la posizione della luce in coordinate di oggetti omogenee. Viene eseguito il mapping diretto dei valori integer e a virgola mobile. Non vengono bloccati né i valori integer né i valori a virgola mobile. <br/> La posizione viene trasformata dalla matrice Modelview quando viene chiamato [**glLightiv**](gllightfv.md) (esattamente come se fosse un punto) ed è archiviata in coordinate oculari. Se il componente *w* della posizione è 0,0, la luce viene considerata come un'origine direzionale. I calcoli di illuminazione diffusa e speculare prendono la direzione della luce, ma non la posizione effettiva, in considerazione e l'attenuazione è disabilitata. In caso contrario, i calcoli di illuminazione diffusa e speculare si basano sulla posizione effettiva della luce nelle coordinate oculari ed è abilitata l'attenuazione. La posizione predefinita è (0, 0, 1, 0); quindi, la sorgente di luce predefinita è direzionale, parallela a e nella direzione dell'asse-*z* .<br/> |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**\_direzione spot \_ GL**</dt> </dl>                                                                                                                                                                          | Il parametro *params* contiene tre valori integer che specificano la direzione della luce nelle coordinate di oggetti omogenee. Viene eseguito il mapping diretto dei valori integer e a virgola mobile. Non vengono bloccati né i valori integer né i valori a virgola mobile. <br/> La direzione spot viene trasformata dall'inverso della matrice Modelview quando viene chiamato **glLightiv** (proprio come se fosse normale) e viene archiviato in coordinate oculari. Si tratta di un valore significativo solo quando GL \_ spot \_ cutoff non è 180, per impostazione predefinita. La direzione predefinita è (0, 0, 1).<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**\_esponente spot GL \_**</dt> </dl>                                                                                                                                                                             | Il parametro *params* è un singolo valore integer che specifica la distribuzione dell'intensità della luce. Viene eseguito il mapping diretto dei valori integer e a virgola mobile. Sono accettati solo i valori nell'intervallo compreso tra \[ 0 e 128 \] . <br/> L'intensità di luce effettiva viene attenuata in base al coseno dell'angolo tra la direzione della luce e la direzione dalla luce al vertice che viene illuminato, elevato alla potenza dell'esponente di spot. Pertanto, gli esponenti di punti più elevati generano una fonte di luce più mirata, indipendentemente dall'angolo di taglio. L'esponente spot predefinito è 0, ottenendo una distribuzione uniforme.<br/>                                                                                                                                                                                                                                                                                                                                          |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**\_taglio GL spot \_**</dt> </dl>                                                                                                                                                                                   | Il parametro *params* è un singolo valore integer che specifica l'angolo massimo della distribuzione di una sorgente di luce. Viene eseguito il mapping diretto dei valori integer e a virgola mobile. Vengono accettati solo i valori compresi tra \[ 0, 90 \] e il valore speciale 180. <br/> Se l'angolo tra la direzione della luce e la direzione dalla luce al vertice che viene illuminato è maggiore dell'angolo di taglio, la luce viene mascherata completamente. In caso contrario, l'intensità viene controllata dall'esponente spot e dai fattori di attenuazione. Il valore predefinito per il punto di interruzione è 180, ottenendo una distribuzione chiara uniforme.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <dt>**\_ \_ attenuazione costante GL, \_ \_ attenuazione lineare GL, \_ attenuazione quadratica GL \_**</dt> </dl> | Il parametro *params* è un singolo valore integer che specifica uno dei tre fattori di attenuazione della luce. Viene eseguito il mapping diretto dei valori integer e a virgola mobile. Vengono accettati solo valori non negativi. <br/> Se la luce è posizionale, anziché direzionale, l'intensità viene attenuata dalla reciproca della somma di: il fattore costante, il fattore lineare moltiplicato per la distanza tra la luce e il vertice che viene illuminato e il fattore quadratico moltiplicato per il quadrato della stessa distanza. I fattori di attenuazione predefiniti sono (1, 0, 0), con conseguente assenza di attenuazione.<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*params* 
</dt> <dd>

Specifica il valore impostato per il parametro *pname* della *luce* sorgente chiara.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *Light* o *pname* non è un valore accettato.<br/>                                                                                                                                                                  |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | Un valore dell'esponente spot è stato specificato al di fuori dell'intervallo compreso tra \[ 0, 128 o l'elemento \] cutoff è stato specificato al di fuori dell'intervallo \[ 0, 90 \] (ad eccezione del valore speciale 180) oppure è stato specificato un fattore di attenuazione negativo.<br/> |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                                                                     |



## <a name="remarks"></a>Commenti

La funzione **glLightiv** imposta il valore o i valori dei singoli parametri della sorgente di luce. Il parametro *Light* denomina la luce e è un nome simbolico del formato GL \_ Light *i*, dove 0 = *i* < GL \_ Max \_ Lights.

Il parametro *pname* specifica uno dei parametri della sorgente di luce, di nuovo in base al nome simbolico. Il parametro *params* può essere un singolo valore o un puntatore a una matrice che contiene i nuovi valori.

Il calcolo dell'illuminazione è abilitato e disabilitato usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l'illuminazione GL degli argomenti \_ . Quando è abilitata l'illuminazione, le sorgenti luminose abilitate contribuiscono al calcolo dell'illuminazione. Source Light *i* è abilitato e disabilitato usando **glEnable** e **glDisable** con l'argomento GL \_ Light *i*.

È sempre il caso GL \_ Light *i* = GL \_ LIGHT0 + *i*.

Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glLightiv** :

[**glGetLight**](glgetlight.md)

[**glIsEnabled**](glisenabled.md) con illuminazione GL argomento \_

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> </dl>

 

 





