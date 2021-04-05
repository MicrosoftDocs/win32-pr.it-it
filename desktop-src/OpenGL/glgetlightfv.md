---
title: funzione glGetLightfv (GL. h)
description: Le funzioni glGetLightfv e glGetLightiv restituiscono valori di parametro di origine Light. | funzione glGetLightfv (GL. h)
ms.assetid: 81049726-426e-4f90-bb8e-e5d467870260
keywords:
- funzione glGetLightfv OpenGL
topic_type:
- apiref
api_name:
- glGetLightfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf90cb9567822ef578bdf01805648a2dabd02db
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886120"
---
# <a name="glgetlightfv-function"></a>glGetLightfv (funzione)

Le funzioni **glGetLightfv** e [**glGetLightiv**](glgetlightiv.md) restituiscono valori di parametro di origine Light.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetLightfv(
   GLenum  light,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*light* 
</dt> <dd>

Sorgente di luce. Il numero di spie possibili dipende dall'implementazione, ma sono supportate almeno otto luci. Sono identificati da nomi simbolici nel formato GL \_ Light *i* where 0 = *i* < GL \_ Max \_ Lights.

</dd> <dt>

*pname* 
</dt> <dd>

Parametro della sorgente di luce per la *luce*. I nomi simbolici seguenti sono accettati.



| Valore                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**\_ambiente GL**</dt> </dl>                                            | Il parametro *params* restituisce quattro valori integer o a virgola mobile che rappresentano l'intensità di ambiente della sorgente di luce. Per i valori integer, quando richiesto, viene eseguito il mapping lineare dalla rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1, 1 \] , il valore restituito intero corrispondente non è definito.<br/>                                                                                                                                                                  |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ diffuse**</dt> </dl>                                            | Il parametro *params* restituisce quattro valori integer o a virgola mobile che rappresentano l'intensità diffusa della sorgente di luce. Per i valori integer, quando richiesto, viene eseguito il mapping lineare dalla rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1, 1 \] , il valore restituito intero corrispondente non è definito.<br/>                                                                                                                                                                  |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_speculare GL**</dt> </dl>                                         | Il parametro *params* restituisce quattro valori integer o a virgola mobile che rappresentano l'intensità speculare della sorgente di luce. Per i valori integer, quando richiesto, viene eseguito il mapping lineare dalla rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1, 1 \] , il valore restituito intero corrispondente non è definito.<br/>                                                                                                                                                                 |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**\_posizione GL**</dt> </dl>                                         | Il parametro *params* restituisce quattro valori integer o a virgola mobile che rappresentano la posizione della sorgente di luce. I valori integer, se richiesti, vengono calcolati mediante l'arrotondamento dei valori a virgola mobile interni al valore intero più vicino. I valori restituiti sono quelli mantenuti in coordinate oculari. Non saranno uguali ai valori specificati tramite [**glLight**](gllight-functions.md), a meno che non sia stata identificata la matrice Modelview al momento della chiamata di **glLight** .<br/>                                                                                                                                                             |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**\_direzione spot \_ GL**</dt> </dl>                      | Il parametro *params* restituisce tre valori integer o a virgola mobile che rappresentano la direzione della sorgente di luce. I valori integer, se richiesti, vengono calcolati mediante l'arrotondamento dei valori a virgola mobile interni al valore intero più vicino. I valori restituiti sono quelli mantenuti in coordinate oculari. Non saranno uguali ai valori specificati tramite **glLight**, a meno che non sia stata identificata la matrice Modelview al momento della chiamata di **glLight** . Sebbene la direzione spot venga normalizzata prima di essere utilizzata nell'equazione di illuminazione, i valori restituiti sono le versioni trasformate dei valori specificati prima della normalizzazione.<br/> |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**\_esponente spot GL \_**</dt> </dl>                         | Il parametro *params* restituisce un singolo valore integer o a virgola mobile che rappresenta l'esponente spot della luce. Un valore integer, quando richiesto, viene calcolato eseguendo l'arrotondamento della rappresentazione a virgola mobile interna all'intero più vicino.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**\_taglio GL spot \_**</dt> </dl>                               | Il parametro *params* restituisce un singolo valore integer o a virgola mobile che rappresenta l'angolo di taglio della luce. Un valore integer, quando richiesto, viene calcolato eseguendo l'arrotondamento della rappresentazione a virgola mobile interna all'intero più vicino.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span><dl> <dt>**\_ \_ attenuazione costante GL**</dt> </dl>    | Il parametro *params* restituisce un singolo valore integer o a virgola mobile che rappresenta l'attenuazione della luce costante (non correlata alla distanza). Un valore integer, quando richiesto, viene calcolato eseguendo l'arrotondamento della rappresentazione a virgola mobile interna all'intero più vicino.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span><dl> <dt>**\_ \_ attenuazione lineare GL**</dt> </dl>          | Il parametro *params* restituisce un singolo valore integer o a virgola mobile che rappresenta l'attenuazione lineare della luce. Un valore integer, quando richiesto, viene calcolato eseguendo l'arrotondamento della rappresentazione a virgola mobile interna all'intero più vicino.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span><dl> <dt>**\_attenuazione quadratica GL \_**</dt> </dl> | Il parametro *params* restituisce un singolo valore integer o a virgola mobile che rappresenta l'attenuazione quadratica della luce. Un valore integer, quando richiesto, viene calcolato eseguendo l'arrotondamento della rappresentazione a virgola mobile interna all'intero più vicino.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*params* 
</dt> <dd>

Restituisce i dati richiesti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **glGetLight** restituisce in *params* il valore o i valori di un parametro della sorgente di luce. Il parametro *Light* denomina la luce e è un nome simbolico del formato GL \_ Light *i* per 0 = *i* < GL \_ Max \_ Lights, dove GL \_ Max \_ Lights è una costante dipendente dall'implementazione che è maggiore o uguale a otto. Il parametro *pname* specifica uno dei dieci parametri di origine luce, di nuovo in base al nome simbolico.

È sempre il caso GL \_ Light *i* = GL \_ LIGHT0 + *i*.

Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *params*.

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

[**Remo**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> </dl>

 

 





