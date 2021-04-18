---
title: funzione glTexEnvi (GL. h)
description: La funzione glTexEnvi imposta un parametro di ambiente di trama.
ms.assetid: 3f4c10c4-524c-4cce-b42b-bc72fc3b9f31
keywords:
- funzione glTexEnvi OpenGL
topic_type:
- apiref
api_name:
- glTexEnvi
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c013b0e4805042ed0967e02df83f143d8bcfd991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301004"
---
# <a name="gltexenvi-function"></a>glTexEnvi (funzione)

La funzione **glTexEnvi** imposta un parametro di ambiente di trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexEnvi(
   GLenum target,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Ambiente di trama. Deve essere una \_ trama GL \_ env.

</dd> <dt>

*pname* 
</dt> <dd>

Nome simbolico di un parametro di ambiente di trama a valore singolo. Deve essere la \_ modalità ENV della trama GL \_ \_ .

</dd> <dt>

*param* 
</dt> <dd>

Una singola costante simbolica, una regola GL \_ Modular, GL \_ decal, GL \_ Blend o GL \_ Replace.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *target* o *pname* non è uno dei valori definiti accettati oppure quando *params* deve avere un valore costante definito (in base al valore di *pname*) e no.<br/> |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/>                                             |



## <a name="remarks"></a>Commenti

Un ambiente di trama specifica come vengono interpretati i valori di trama quando si crea una trama di un frammento. Il parametro di *destinazione* deve essere un GL \_ texture \_ env. Il parametro *pname* è la \_ \_ modalità ENV texture env \_ . Sono definite tre funzioni di trama, ovvero i \_ modulari GL, GL \_ decal e GL \_ Blend.

Una funzione di trama agisce sul frammento per creare una trama usando il valore dell'immagine di trama che si applica al frammento (vedere [**glTexParameter**](gltexparameter-functions.md)) e produce un colore RGBA per tale frammento. La tabella seguente illustra come viene prodotto il colore RGBA per ognuna delle tre funzioni di trama che è possibile scegliere. *C* è una tripla di valori di colore (RGB) e *un* è il valore alfa associato. I valori RGBA estratti da un'immagine di trama sono compresi nell'intervallo compreso tra \[ 0 e 1 \] . Il pedice *f* fa riferimento al frammento in ingresso, ovvero l'indice *t* nell'immagine di trama, il pedice *c* nel colore dell'ambiente di trama e l'indice *v* indica un valore prodotto dalla funzione texture.

Un'immagine di trama può avere fino a quattro componenti per ogni elemento di trama (vedere [**glTexImage1D**](glteximage1d.md) e [**glTexImage2D**](glteximage2d.md)). In un'immagine a un componente, lt indica il singolo componente. Un'immagine A due componenti usa *L?*  e *un?* . Un'immagine a tre componenti ha solo un valore di colore, *C?* . Un'immagine a quattro componenti presenta un valore di colore *C?*  e un valore alfa *A?* .



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
<td rowspan="2">1 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">$ {REMOVE} $ non definito<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em> <em>) C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></td>
<td><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">2 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">$ {REMOVE} $ non definito<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em> <em>) C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></td>
<td><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">3 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em></td>
<td rowspan="2">$ {REMOVE} $ non definito<br />
</td>
</tr>
<tr class="even">
<td><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em> </td>
<td><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">4 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em> = (1- <em>A?</em> <em>) C<sub>f</sub> </em> + <em>A?</em> <em>C?</em></td>
<td rowspan="2">$ {REMOVE} $ non definito<br />
</td>
</tr>
<tr class="even">
<td><em><sub>V</sub> </em>  =  <em>A?</em> <em><sub>F</sub></em> </td>
<td><em><sub>V</sub> </em>  =  <em><sub>F</sub> </em></td>


</tr>
</tbody>
</table>



 

\_ \_ Per impostazione predefinita, la modalità ENV della trama GL viene \_ \_ modulata.

La funzione seguente recupera le informazioni correlate a **glTexEnvi**:

[**glTexGetEnviv**](glgettexenviv.md)

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





