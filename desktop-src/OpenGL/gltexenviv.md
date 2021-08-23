---
title: Funzione glTexEnviv (Gl.h)
description: La funzione glTexEnviv imposta un parametro di ambiente texture.
ms.assetid: e98ce736-cc68-4687-8c1b-6b0fef7a677a
keywords:
- Funzione glTexEnviv OpenGL
topic_type:
- apiref
api_name:
- glTexEnviv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d77cee8aeec55aa09ead5df227fd018d14d6682e08a047d40a1121a11839083
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519761"
---
# <a name="gltexenviv-function"></a>Funzione glTexEnviv

La **funzione glTexEnviv imposta** un parametro di ambiente texture.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexEnviv(
         GLenum target,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Ambiente di trama. Deve essere GL \_ TEXTURE \_ ENV.

</dd> <dt>

*Pname* 
</dt> <dd>

Nome simbolico di un parametro dell'ambiente di trama a valore singolo. I valori accettati sono GL \_ TEXTURE ENV MODE e GL TEXTURE ENV \_ \_ \_ \_ \_ COLOR.

</dd> <dt>

*params* 
</dt> <dd>

Puntatore a una matrice di parametri: una singola costante simbolica o un colore RGBA.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *target* o *pname* non è uno dei valori definiti accettati o quando *params* deve avere un valore costante definito (in base al valore *di pname*) e non lo ha fatto.<br/> |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                             |



## <a name="remarks"></a>Commenti

Un ambiente di trama specifica come vengono interpretati i valori della trama quando viene con trama un frammento. Il *parametro di* destinazione deve essere GL TEXTURE \_ \_ ENV. Il *parametro pname* può essere GL \_ TEXTURE ENV MODE o GL TEXTURE ENV \_ \_ \_ \_ \_ COLOR.

Se *pname* è GL \_ TEXTURE ENV \_ \_ MODE, *params* è (o punta a) il nome simbolico di una funzione di trama. Sono definite tre funzioni di trama: GL \_ MODULATE, GL \_ DECAL e GL \_ BLEND.

Una funzione di trama agisce sul frammento da trame usando il valore dell'immagine della trama che si applica al frammento (vedere [**glTexParameter)**](gltexparameter-functions.md)e produce un colore RGBA per tale frammento. La tabella seguente illustra come viene prodotto il colore RGBA per ognuna delle tre funzioni di trama che è possibile scegliere. *C* è una tripla di valori di colore (RGB) *e A* è il valore alfa associato. I valori RGBA estratti da un'immagine di trama sono \[ nell'intervallo 0, 1 \] . L'indice *f* fa riferimento al frammento in ingresso, l'indice *t* all'immagine della trama, l'indice *c* al colore dell'ambiente della trama e l'indice *v* indica un valore prodotto dalla funzione texture.

Un'immagine di trama può avere fino a quattro componenti per ogni elemento della trama (vedere [**glTexImage1D**](glteximage1d.md) e [**glTexImage2D).**](glteximage2d.md) In un'immagine con un solo componente, Lt indica il singolo componente. Un'immagine a due componenti usa *L?*  e *A?* . Un'immagine a tre componenti ha solo un valore di colore, *C?* . Un'immagine a quattro componenti ha entrambi un valore di colore *C?*  e un valore alfa *A?* .



<table>
<thead>
<tr class="header">
<th>Numero di componenti</th>
<th>GL_MODULATE</th>
<th>GL_DECAL</th>
<th>GL_BLEND</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">1${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em> <em>)C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">2${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L?</em> <em>)C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">3${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em>   =  <em>C?</em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em> </td>
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">4${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>   =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em> = (1 - <em>A?</em> <em>)C<sub>f</sub> </em> + <em>A?</em> <em>C?</em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>   =  <em>A?</em> <em>A<sub>f</sub></em> </td>
<td><em>A<sub>v</sub> </em>   =  <em>A<sub>f</sub> </em></td>


</tr>
</tbody>
</table>



 

Se pname è GL TEXTURE ENV COLOR, params è un puntatore a una matrice che contiene un \_ \_ colore \_ RGBA costituito da quattro valori.  I componenti di colore integer vengono interpretati in modo lineare in modo che il numero intero più positivo sia mappato a 1,0 e il numero intero più negativo venga mappato a -1,0. I valori vengono definiti nell'intervallo \[ 0, 1 \] quando vengono specificati. *C <sub>c</sub>* accetta questi quattro valori.

L'impostazione predefinita di GL TEXTURE ENV MODE è GL MODULATE e GL TEXTURE ENV COLOR è \_ \_ \_ \_ \_ \_ \_ (0, 0, 0, 0).

La funzione seguente recupera le informazioni correlate **a glTexEnviv:**

[**glTexGetEnviv**](glgettexenviv.md)

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





