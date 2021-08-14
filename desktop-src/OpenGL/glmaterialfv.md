---
title: Funzione glMaterialfv (Gl.h)
description: La funzione glMaterialfv specifica i parametri dei materiali per il modello di illuminazione.
ms.assetid: cd357686-4d6f-49fd-a111-308b5485ac21
keywords:
- Funzione glMaterialfv OpenGL
topic_type:
- apiref
api_name:
- glMaterialfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c4d8fc3f1e141f9913fe997da0b9982200f6be77edc5e4ef190970ee2fca87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358949"
---
# <a name="glmaterialfv-function"></a>Funzione glMaterialfv

La **funzione glMaterialfv** specifica i parametri dei materiali per il modello di illuminazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glMaterialfv(
         GLenum  face,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Faccia* 
</dt> <dd>

Viso o visi da aggiornare. Deve essere uno dei seguenti: GL \_ FRONT, GL \_ BACK o GL FRONT e GL \_ \_ BACK.

</dd> <dt>

*Pname* 
</dt> <dd>

Parametro material del viso o dei visi da aggiornare. I parametri che possono essere specificati usando **glMaterialfv** e le relative interpretazioni dall'equazione di illuminazione sono i seguenti.



| Valore                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**AMBIENTE \_ GL**</dt> </dl>                                       | Il parametro params contiene quattro valori a virgola mobile che specificano la riflessa RGBA di ambiente del materiale. I valori interi vengono mappati in modo lineare in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo a -1,0. I valori a virgola mobile vengono mappati direttamente. Né i valori integer né i valori a virgola mobile sono di tipo "clamped". La riflettore ambientale predefinita per i materiali anteriore e posteriore è (0.2, 0.2, 0.2, 1.0). <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFFUSE**</dt> </dl>                                       | Il parametro params contiene quattro valori a virgola mobile che specificano la riflessa RGBA diffusa del materiale. I valori interi vengono mappati in modo lineare in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo a -1,0. I valori a virgola mobile vengono mappati direttamente. Né i valori integer né i valori a virgola mobile sono di tipo "clamped". La riflettore diffusa predefinita per i materiali anteriore e posteriore è (0.8, 0.8, 0.8, 1.0). <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**SPECULARE GL \_**</dt> </dl>                                    | Il parametro params contiene quattro valori a virgola mobile che specificano la riflessa RGBA speculare del materiale. I valori interi vengono mappati in modo lineare in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo a -1,0. I valori a virgola mobile vengono mappati direttamente. Né i valori integer né i valori a virgola mobile sono di tipo "clamped". La riflettenza speculare predefinita per i materiali anteriore e posteriore è (0.0, 0.0, 0.0, 1.0). <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**EMISSIONE GL \_**</dt> </dl>                                    | Il parametro params contiene quattro valori a virgola mobile che specificano l'intensità della luce emessa da RGBA del materiale. I valori interi vengono mappati in modo lineare in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo a -1,0. I valori a virgola mobile vengono mappati direttamente. Né i valori integer né i valori a virgola mobile sono di tipo "clamped". L'intensità di emissione predefinita per i materiali anteriore e posteriore è (0.0, 0.0, 0.0, 1.0). <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**GL \_ SHININESS**</dt> </dl>                                 | Il *parametro param* è un singolo valore intero che specifica l'esponente speculare RGBA del materiale. I valori interi vengono mappati direttamente. Vengono accettati solo i \[ valori nell'intervallo 0, 128. \] L'esponente speculare predefinito per i materiali anteriore e posteriore è 0. <br/>                                                                                                                                                                                                      |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <dt>**GL \_ AMBIENTE \_ E \_ DIFFUSIONE**</dt> </dl> | Equivale a chiamare [**glMaterial due**](glmaterial-functions.md) volte con gli stessi valori di parametro, una con GL \_ AMBIENT e una con GL \_ DIFFUSE. <br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**INDICI COLORI GL \_ \_**</dt> </dl>                    | Il parametro params contiene tre valori a virgola mobile che specificano gli indici dei colori per l'illuminazione ambientale, diffusa e speculare. Questi tre valori, GL EREALITÀ, sono gli unici valori di materiale usati dall'equazione di illuminazione in modalità indice \_ colori. Per una descrizione dell'illuminazione dell'indice dei colori, vedere [**glLightModel.**](gllightmodel-functions.md)<br/>                                                                                                                                  |



 

</dd> <dt>

*params* 
</dt> <dd>

Valore sul quale verrà impostato il parametro \_ GL GL GLINESS.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                              | Significato                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>  | Viso *o* *pname non* è un valore accettato.<br/>                |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl> | È stato specificato un esponente speculare non compreso \[ nell'intervallo 0, 128. \]<br/> |



## <a name="remarks"></a>Commenti

La [**funzione glMaterialfv**](glmaterialf.md) assegna valori ai parametri material. Esistono due set corrispondenti di parametri di materiale. Uno, il *set* anteriore, viene usato per ombreggiatura di punti, linee, bitmap e tutti i poligoni (quando l'illuminazione a due lati è disabilitata) o solo per i poligoni frontali (quando è abilitata l'illuminazione fronte-lato). L'altro set, *rivolto all'indietro,* viene usato per ombreggiaturare i poligoni rivolti all'indietro solo quando è abilitata l'illuminazione a due lati. Fare riferimento [**a glLightModel**](gllightmodel-functions.md) per informazioni dettagliate sui calcoli dell'illuminazione su un lato e su due lati.

La [**funzione glMaterialfv**](glmaterialf.md) accetta tre argomenti. Il primo, *viso,* specifica se i materiali GL FRONT, GL BACK o entrambi i materiali \_ GL FRONT e BACK verranno \_ \_ \_ \_ modificati. Il secondo, *pname*, specifica quale dei diversi parametri in uno o entrambi i set verrà modificato. Il terzo, *param*, specifica il valore che verrà assegnato al parametro specificato.

I parametri dei materiali vengono usati nell'equazione di illuminazione che viene facoltativamente applicata a ogni vertice. L'equazione viene illustrata in [**glLightModel**](gllightmodel-functions.md).

I parametri del materiale possono essere aggiornati in qualsiasi momento. In particolare, [**è possibile chiamare glMaterialfv**](glmaterialf.md) tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). Se è necessario modificare un solo parametro material per vertice, tuttavia, [**glColorMaterial**](glcolormaterial.md) è preferibile rispetto **a glMaterialfv**.

La funzione seguente recupera le informazioni correlate a [**glMaterialfv**](glmaterialf.md):

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





