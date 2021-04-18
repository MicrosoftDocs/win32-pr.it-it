---
title: funzione glMaterialiv (GL. h)
description: La funzione glMaterialiv specifica i parametri del materiale per il modello di illuminazione.
ms.assetid: 9d045202-e565-4cf7-946a-60299e1bc1b1
keywords:
- funzione glMaterialfv OpenGL
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
ms.openlocfilehash: 95f12a5d34357a3436ffd6725ad2f1d56901e700
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400528"
---
# <a name="glmaterialiv-function"></a>glMaterialiv (funzione)

La funzione **glMaterialiv** specifica i parametri del materiale per il modello di illuminazione.

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

*faccia* 
</dt> <dd>

Il volto o i visi da aggiornare. Deve essere uno dei seguenti: GL \_ Front, GL \_ back o GL \_ front e GL \_ back.

</dd> <dt>

*pname* 
</dt> <dd>

Il parametro Material della faccia o dei visi da aggiornare. I parametri che possono essere specificati tramite [**glMaterialiv**](glmaterialfv.md)e le relative interpretazioni dall'equazione di illuminazione sono i seguenti.



| Valore                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**\_ambiente GL**</dt> </dl>                                       | Il parametro params contiene quattro valori integer che specificano la reflection RGBA di ambiente del materiale. Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0. Ai valori a virgola mobile viene eseguito il mapping diretto. Non vengono bloccati né i valori integer né i valori a virgola mobile. La reflection di ambiente predefinita per i materiali front-end e di back-end è (0,2, 0,2, 0,2, 1,0). <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ diffuse**</dt> </dl>                                       | Il parametro params contiene quattro valori integer che specificano la reflection RGBA diffusa del materiale. Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0. Ai valori a virgola mobile viene eseguito il mapping diretto. Non vengono bloccati né i valori integer né i valori a virgola mobile. La reflection predefinita diffusa sia per i materiali front-end che per quelli di back-end è (0,8, 0,8, 0,8, 1,0). <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**\_speculare GL**</dt> </dl>                                    | Il parametro params contiene quattro valori integer che specificano la reflection RGBA speculare del materiale. Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0. Ai valori a virgola mobile viene eseguito il mapping diretto. Non vengono bloccati né i valori integer né i valori a virgola mobile. La reflection speculare predefinita sia per i materiali front-end che per quelli di back-end è (0,0, 0,0, 0,0, 1,0). <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**\_emissione GL**</dt> </dl>                                    | Il parametro params contiene quattro valori integer che specificano l'intensità della luce emessa dal RGBA del materiale. Ai valori integer viene eseguito il mapping lineare, in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentativo più negativo sia mappato a-1,0. Ai valori a virgola mobile viene eseguito il mapping diretto. Non vengono bloccati né i valori integer né i valori a virgola mobile. L'intensità di emissione predefinita per i materiali front-end e di back-end è (0,0, 0,0, 0,0, 1,0). <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_lucentezza GL**</dt> </dl>                                 | Il parametro *param* è un singolo integer che specifica l'esponente speculare RGBA del materiale. Viene eseguito il mapping diretto dei valori integer. Sono accettati solo i valori nell'intervallo compreso tra \[ 0 e 128 \] . L'esponente speculare predefinito per i materiali front-end e di back-end è 0. <br/>                                                                                                                                                                                                     |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <dt>**\_ambiente GL \_ e \_ diffusa**</dt> </dl> | Equivale a chiamare due volte [**glMaterial**](glmaterial-functions.md) con gli stessi valori di parametro, una volta con l' \_ ambiente GL e una volta con GL \_ Diffusion. <br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**indici di \_ colore GL \_**</dt> </dl>                    | Il parametro params contiene tre valori integer che specificano gli indici dei colori per l'illuminazione ambientale, diffusa e speculare. Questi tre valori, e GL \_ lucentezza, sono gli unici valori di materiale usati dall'equazione di illuminazione della modalità di indice dei colori. Per informazioni sull'illuminazione degli indici dei colori, vedere [**glLightModel**](gllightmodel-functions.md) .<br/>                                                                                                                                  |



 

</dd> <dt>

*params* 
</dt> <dd>

Valore in cui verrà impostato il parametro GL \_ lucentezza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                              | Significato                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>  | *Face* o *pname* non è un valore accettato.<br/>                |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl> | È stato specificato un esponente speculare non compreso nell'intervallo \[ 0, 128 \] .<br/> |



## <a name="remarks"></a>Commenti

La funzione [**glMaterialiv**](glmaterialf.md) assegna valori ai parametri del materiale. Sono disponibili due set di parametri Material corrispondenti. Uno, il set in *primo piano* , viene usato per ombreggiare punti, linee, bitmap e tutti i poligoni (quando l'illuminazione bilaterale è disabilitata) o solo i poligoni di fronte (quando è abilitata l'illuminazione bilaterale). L'altro set, *back-facing*, viene usato per ombreggiare i poligoni di back-end solo quando è abilitata l'illuminazione a due lati. Per informazioni dettagliate sui calcoli di illuminazione unilaterale e bilaterale, vedere [**glLightModel**](gllightmodel-functions.md) .

La funzione [**glMaterialiv**](glmaterialf.md) accetta tre argomenti. Il *primo, ovvero, specifica* se i materiali di contabilità GL \_ , i \_ materiali back GL o entrambi i \_ materiali GL front \_ e \_ back verranno modificati. Il secondo, *pname*, specifica quale dei diversi parametri in uno o entrambi i set verranno modificati. Il *terzo parametro specifica* il valore che verrà assegnato al parametro specificato.

I parametri del materiale vengono usati nell'equazione di illuminazione applicata facoltativamente a ogni vertice. L'equazione viene illustrata in [**glLightModel**](gllightmodel-functions.md).

I parametri Material possono essere aggiornati in qualsiasi momento. In particolare, è possibile chiamare [**glMaterialiv**](glmaterialf.md) tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). Se è necessario modificare un solo parametro Material per ogni vertice, tuttavia, [**glColorMaterial**](glcolormaterial.md) è preferibile rispetto a **glMaterialiv**.

La funzione seguente recupera le informazioni correlate a [**glMaterialiv**](glmaterialf.md):

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





