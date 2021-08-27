---
title: Funzione glMaterialiv (Gl.h)
description: La funzione glMaterialiv specifica i parametri del materiale per il modello di illuminazione.
ms.assetid: 9d045202-e565-4cf7-946a-60299e1bc1b1
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
ms.openlocfilehash: 922fd0cd90b848f0d5c324451f502faa8fa6b961686b209cb881c752b992a6df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128211"
---
# <a name="glmaterialiv-function"></a>Funzione glMaterialiv

La **funzione glMaterialiv** specifica i parametri del materiale per il modello di illuminazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glMaterialfv(
         GLenum face,
         GLenum pname,
   const GLint  *params
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

Parametro material del viso o dei visi da aggiornare. I parametri che possono essere specificati usando [**glMaterialiv**](glmaterialfv.md)e le relative interpretazioni dall'equazione di illuminazione sono i seguenti.



| Valore                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**AMBIENTE \_ GL**</dt> </dl>                                       | Il parametro params contiene quattro valori integer che specificano la riflettenza RGBA di ambiente del materiale. I valori interi vengono mappati in modo lineare in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo sia mappato a -1,0. I valori a virgola mobile vengono mappati direttamente. Né i valori integer né i valori a virgola mobile sono a virgola mobile. La riflettenza di ambiente predefinita per i materiali front-facing e back-facing è (0.2, 0.2, 0.2, 1.0). <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFFUSE**</dt> </dl>                                       | Il parametro params contiene quattro valori integer che specificano la riflessa RGBA diffusa del materiale. I valori interi vengono mappati in modo lineare in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo sia mappato a -1,0. I valori a virgola mobile vengono mappati direttamente. Né i valori integer né i valori a virgola mobile sono a virgola mobile. La riflettore diffusa predefinita per i materiali front-facing e back-facing è (0,8, 0.8, 0.8, 1.0). <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_SPECULARE GL**</dt> </dl>                                    | Il parametro params contiene quattro valori interi che specificano la riflettenza speculare RGBA del materiale. I valori interi vengono mappati in modo lineare in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo sia mappato a -1,0. I valori a virgola mobile vengono mappati direttamente. Né i valori integer né i valori a virgola mobile sono a virgola mobile. La riflettenza speculare predefinita per i materiali front-facing e back-facing è (0.0, 0.0, 0.0, 1.0). <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**EMISSIONE \_ GL**</dt> </dl>                                    | Il parametro params contiene quattro valori interi che specificano l'intensità della luce emessa da RGBA del materiale. I valori interi vengono mappati in modo lineare in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo sia mappato a -1,0. I valori a virgola mobile vengono mappati direttamente. Né i valori integer né i valori a virgola mobile sono a virgola mobile. L'intensità di emissione predefinita per i materiali front-facing e back-facing è (0.0, 0.0, 0.0, 1.0). <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**GL \_ BRILLANTEZZA**</dt> </dl>                                 | Il *parametro param* è un singolo numero intero che specifica l'esponente speculare RGBA del materiale. I valori interi vengono mappati direttamente. Vengono accettati solo i \[ valori nell'intervallo 0, 128. \] L'esponente speculare predefinito per i materiali front-facing e back-facing è 0. <br/>                                                                                                                                                                                                     |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <dt>**AMBIENTE \_ GL \_ E \_ DIFFUSE**</dt> </dl> | Equivale a chiamare [**glMaterial due**](glmaterial-functions.md) volte con gli stessi valori di parametro, una con GL \_ AMBIENT e una con GL \_ DIFFUSE. <br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**INDICI \_ DEI \_ COLORI GL**</dt> </dl>                    | Il parametro params contiene tre valori interi che specificano gli indici dei colori per l'illuminazione ambiente, diffusa e speculare. Questi tre valori, GL SHININESS, sono gli unici valori di materiale usati dall'equazione di illuminazione in modalità \_ indice colori. Per una descrizione dell'illuminazione dell'indice dei colori, vedere [**glLightModel.**](gllightmodel-functions.md)<br/>                                                                                                                                  |



 

</dd> <dt>

*params* 
</dt> <dd>

Valore sul quale verrà impostato il parametro GL \_ SHININESS.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                              | Significato                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>  | Viso *o* *pname non* è un valore accettato.<br/>                |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl> | È stato specificato un esponente speculare non compreso nell'intervallo \[ 0, 128. \]<br/> |



## <a name="remarks"></a>Commenti

La [**funzione glMaterialiv**](glmaterialf.md) assegna valori ai parametri material. Esistono due set corrispondenti di parametri di materiale. Uno, il *set* frontale, viene usato per ombreggiatura di punti, linee, bitmap e tutti i poligoni (quando l'illuminazione a due lati è disabilitata) o solo poligoni frontali (quando è abilitata l'illuminazione a due lati). L'altro set, *rivolto all'indietro,* viene usato per ombreggiatura dei poligoni rivolti verso il retro solo quando è abilitata l'illuminazione a due lati. Fare riferimento [**a glLightModel**](gllightmodel-functions.md) per informazioni dettagliate sui calcoli dell'illuminazione a lato e a due lati.

La [**funzione glMaterialiv**](glmaterialf.md) accetta tre argomenti. Il primo, *viso*, specifica se i materiali GL FRONT, i materiali GL BACK o entrambi i materiali \_ GL FRONT e BACK verranno \_ \_ \_ \_ modificati. Il secondo, *pname*, specifica quale dei diversi parametri in uno o entrambi i set verrà modificato. Il terzo *parametro, param*, specifica il valore che verrà assegnato al parametro specificato.

I parametri dei materiali vengono usati nell'equazione di illuminazione che viene facoltativamente applicata a ogni vertice. L'equazione è descritta in [**glLightModel**](gllightmodel-functions.md).

I parametri del materiale possono essere aggiornati in qualsiasi momento. In particolare, [**glMaterialiv**](glmaterialf.md) può essere chiamato tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). Se è necessario modificare un solo parametro materiale per vertice, tuttavia, [**glColorMaterial**](glcolormaterial.md) è preferibile rispetto **a glMaterialiv**.

La funzione seguente recupera le informazioni correlate a [**glMaterialiv**](glmaterialf.md):

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

 

 





