---
title: Funzione glGetLightfv (Gl.h)
description: Le funzioni glGetLightfv e glGetLightiv restituiscono valori di parametro di origine chiaro. | Funzione glGetLightfv (Gl.h)
ms.assetid: 81049726-426e-4f90-bb8e-e5d467870260
keywords:
- Funzione glGetLightfv OpenGL
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
ms.openlocfilehash: 5d642b0d253abca4ea7c5f224353f5544b5307df5237e958c32e37b98ff2e01f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741999"
---
# <a name="glgetlightfv-function"></a>Funzione glGetLightfv

Le **funzioni glGetLightfv** e [**glGetLightiv**](glgetlightiv.md) restituiscono valori di parametro di origine chiaro.

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

Una sorgente di luce. Il numero di possibili luci dipende dall'implementazione, ma sono supportate almeno otto luci. Sono identificati da nomi simbolici nel formato GL \_ LIGHT *i* dove 0 = *i <* GL \_ MAX \_ LIGHTS.

</dd> <dt>

*Pname* 
</dt> <dd>

Parametro della sorgente di luce per *light*. Vengono accettati i nomi simbolici seguenti.



| Valore                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**AMBIENTE \_ GL**</dt> </dl>                                            | Il *parametro params* restituisce quattro valori interi o a virgola mobile che rappresentano l'intensità di ambiente della sorgente di luce. I valori interi, se richiesti, vengono mappati in modo lineare dalla rappresentazione a virgola mobile interna in modo che 1.0 eseere mappato al valore integer rappresentabile più positivo e -1.0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1,1, \] il valore restituito intero corrispondente non è definito.<br/>                                                                                                                                                                  |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFFUSE**</dt> </dl>                                            | Il *parametro params* restituisce quattro valori interi o a virgola mobile che rappresentano l'intensità diffusa della sorgente di luce. I valori interi, se richiesti, vengono mappati in modo lineare dalla rappresentazione a virgola mobile interna in modo che 1.0 eseere mappato al valore integer rappresentabile più positivo e -1.0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1,1, \] il valore restituito intero corrispondente non è definito.<br/>                                                                                                                                                                  |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_SPECULARE GL**</dt> </dl>                                         | Il *parametro params* restituisce quattro valori interi o a virgola mobile che rappresentano l'intensità speculare della sorgente di luce. I valori interi, se richiesti, vengono mappati in modo lineare dalla rappresentazione a virgola mobile interna in modo che 1.0 eseere mappato al valore integer rappresentabile più positivo e -1.0 sia mappato al valore integer rappresentabile più negativo. Se il valore interno non è compreso nell'intervallo \[ -1,1, \] il valore restituito intero corrispondente non è definito.<br/>                                                                                                                                                                 |
| <span id="GL_POSITION"></span><span id="gl_position"></span><dl> <dt>**POSIZIONE \_ DI CONTABILITÀ GENERALE**</dt> </dl>                                         | Il *parametro params* restituisce quattro valori integer o a virgola mobile che rappresentano la posizione della sorgente di luce. I valori interi, se richiesti, vengono calcolati arrotondando i valori a virgola mobile interni al valore intero più vicino. I valori restituiti sono quelli mantenuti in coordinate oculare. Non saranno uguali ai valori specificati tramite [**glLight**](gllight-functions.md), a meno che la matrice modelview non sia stata identificata al momento della chiamata **di glLight.**<br/>                                                                                                                                                             |
| <span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span><dl> <dt>**DIREZIONE \_ DEL PUNTO \_ GL**</dt> </dl>                      | Il *parametro params* restituisce tre valori interi o a virgola mobile che rappresentano la direzione della sorgente di luce. I valori interi, se richiesti, vengono calcolati arrotondando i valori a virgola mobile interni al valore intero più vicino. I valori restituiti sono quelli mantenuti in coordinate oculare. Non saranno uguali ai valori specificati tramite **glLight**, a meno che la matrice modelview non sia stata identificata al momento della chiamata **di glLight.** Anche se la direzione del punto viene normalizzata prima di essere usata nell'equazione di illuminazione, i valori restituiti sono le versioni trasformate dei valori specificati prima della normalizzazione.<br/> |
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <dt>**ESPONENTE DI GL \_ SPOT \_**</dt> </dl>                         | Il *parametro params* restituisce un singolo valore intero o a virgola mobile che rappresenta l'esponente spot della luce. Un valore intero, quando richiesto, viene calcolato arrotondando la rappresentazione a virgola mobile interna all'intero più vicino.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <dt>**GL \_ SPOT \_ CUTOFF**</dt> </dl>                               | Il *parametro params* restituisce un singolo valore intero o a virgola mobile che rappresenta l'angolo di taglio spot della luce. Un valore intero, quando richiesto, viene calcolato arrotondando la rappresentazione a virgola mobile interna all'intero più vicino.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span><dl> <dt>**ATTENUAZIONE COSTANTE GL \_ \_**</dt> </dl>    | Il *parametro params* restituisce un singolo valore integer o a virgola mobile che rappresenta l'attenuazione costante (non correlata alla distanza) della luce. Un valore intero, quando richiesto, viene calcolato arrotondando la rappresentazione a virgola mobile interna all'intero più vicino.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span><dl> <dt>**ATTENUAZIONE \_ \_ LINEARE GL**</dt> </dl>          | Il *parametro params* restituisce un singolo valore integer o a virgola mobile che rappresenta l'attenuazione lineare della luce. Un valore intero, quando richiesto, viene calcolato arrotondando la rappresentazione a virgola mobile interna all'intero più vicino.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span><dl> <dt>**\_ATTENUAZIONE \_ QUADRATICA GL**</dt> </dl> | Il *parametro params* restituisce un singolo valore intero o a virgola mobile che rappresenta l'attenuazione quadratica della luce. Un valore intero, quando richiesto, viene calcolato arrotondando la rappresentazione a virgola mobile interna all'intero più vicino.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*params* 
</dt> <dd>

Restituisce i dati richiesti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione glGetLight** restituisce in *params* il valore o i valori di un parametro light source. Il  parametro light denota la luce e è un nome simbolico nel formato GL LIGHT i per \_ 0 = *i* < GL MAX LIGHTS, dove GL MAX LIGHTS è una costante dipendente dall'implementazione maggiore o uguale a \_ \_ \_ \_ otto. Il *parametro pname* specifica uno dei dieci parametri della sorgente di luce, sempre in base al nome simbolico.

È sempre il caso che GL \_ LIGHT *i* = GL \_ LIGHT0 + *i*.

Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *params*.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> </dl>

 

 





