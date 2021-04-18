---
title: funzione glMaterialf (GL. h)
description: La funzione glMaterialf specifica i parametri del materiale per il modello di illuminazione.
ms.assetid: c6d183c4-2d1f-4fb9-b24f-c132ebfc708d
keywords:
- funzione glMaterialf OpenGL
topic_type:
- apiref
api_name:
- glMaterialf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c77cb1be5595f4a872988bbc6480d4cd6f65aae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302624"
---
# <a name="glmaterialf-function"></a>glMaterialf (funzione)

La funzione **glMaterialf** specifica i parametri del materiale per il modello di illuminazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glMaterialf(
   GLenum  face,
   GLenum  pname,
   GLfloat param
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

Parametro Material a valore singolo della faccia o delle facce da aggiornare. Deve essere GL \_ lucentezza.



| Valore                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_lucentezza GL**</dt> </dl> | Il parametro *param* è un singolo valore a virgola mobile che specifica l'esponente speculare RGBA del materiale. Viene eseguito il mapping diretto dei valori integer. Sono accettati solo i valori nell'intervallo compreso tra \[ 0 e 128 \] . L'esponente speculare predefinito per i materiali front-end e di back-end è 0. <br/> |



 

</dd> <dt>

*param* 
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

La funzione **glMaterialf** assegna valori ai parametri del materiale. Sono disponibili due set di parametri Material corrispondenti. Uno, il set in *primo piano* , viene usato per ombreggiare punti, linee, bitmap e tutti i poligoni (quando l'illuminazione bilaterale è disabilitata) o solo i poligoni di fronte (quando è abilitata l'illuminazione bilaterale). L'altro set, *back-facing*, viene usato per ombreggiare i poligoni di back-end solo quando è abilitata l'illuminazione a due lati. Per informazioni dettagliate sui calcoli di illuminazione unilaterale e bilaterale, vedere [**glLightModel**](gllightmodel-functions.md) .

La funzione **glMaterialf** accetta tre argomenti. Il *primo, ovvero, specifica* se i materiali di contabilità GL \_ , i \_ materiali back GL o entrambi i \_ materiali GL front \_ e \_ back verranno modificati. Il secondo, *pname*, specifica quale dei diversi parametri in uno o entrambi i set verranno modificati. Il *terzo parametro specifica* il valore che verrà assegnato al parametro specificato.

I parametri del materiale vengono usati nell'equazione di illuminazione applicata facoltativamente a ogni vertice. L'equazione viene illustrata in [**glLightModel**](gllightmodel-functions.md).

I parametri Material possono essere aggiornati in qualsiasi momento. In particolare, è possibile chiamare **glMaterialf** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). Se è necessario modificare un solo parametro Material per ogni vertice, tuttavia, [**glColorMaterial**](glcolormaterial.md) è preferibile rispetto a **glMaterialf**.

La funzione seguente recupera le informazioni correlate a **glMaterialf**:

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

 

 





