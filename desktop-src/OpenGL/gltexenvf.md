---
title: Funzione glTexEnvf (Gl.h)
description: La funzione glTexEnvf imposta un parametro di ambiente texture.
ms.assetid: 1b203240-a963-4dfe-96bc-735720e16122
keywords:
- Funzione glTexEnvf OpenGL
topic_type:
- apiref
api_name:
- glTexEnvf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4914ae05496c0234adb0b6604f4f75eb630af525b08ccae2825e032d5f97535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613653"
---
# <a name="gltexenvf-function"></a>Funzione glTexEnvf

La **funzione glTexEnvf** imposta un parametro di ambiente texture.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexEnvf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
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

Nome simbolico di un parametro dell'ambiente di trama a valore singolo. Deve essere GL \_ TEXTURE \_ ENV \_ MODE.

</dd> <dt>

*param* 
</dt> <dd>

Singola costante simbolica, una tra GL \_ MODULATE, GL \_ DECAL, GL \_ BLEND o GL \_ REPLACE.

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

Un ambiente di trama specifica come vengono interpretati i valori della trama quando viene con trama un frammento. Il *parametro di* destinazione deve essere GL TEXTURE \_ \_ ENV. Il *parametro pname* è GL \_ TEXTURE ENV \_ \_ MODE. Sono definite tre funzioni di trama: GL \_ MODULATE, GL \_ DECAL e GL \_ BLEND.

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
<td><em>C<sub>v</sub> </em>  =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
<td><em>C</em> <em><sub>v</sub></em>  =  <em>(1</em> - <em>L?</em> <em>)C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">2${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em> <em>)C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">3${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em> </td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">4${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em> = (1 - <em>A?</em> <em>)C<sub>f</sub> </em> + <em>A?</em> <em>C?</em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A?</em> <em>A<sub>f</sub></em> </td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
</tbody>
</table>



 

\_L'impostazione predefinita di GL TEXTURE ENV MODE è GL \_ \_ \_ MODULATE.

La funzione seguente recupera le informazioni correlate **a glTexEnvf**:

[**glTexGetEnvfv**](glgettexenvfv.md)

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

 

 





