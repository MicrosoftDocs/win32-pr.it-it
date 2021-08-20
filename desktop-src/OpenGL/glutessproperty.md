---
title: Funzione gluTessProperty (Glu.h)
description: La funzione gluTessProperty imposta la proprietà di un oggetto a tassellamento.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- Funzione gluTessProperty OpenGL
topic_type:
- apiref
api_name:
- gluTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595139b91e0fb19ac6ef479831604663dea1981e401aa807ba2bb3cd24a29a41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488431"
---
# <a name="glutessproperty-function"></a>Funzione gluTessProperty

La **funzione gluTessProperty** imposta la proprietà di un oggetto a tassellamento.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tess* 
</dt> <dd>

Oggetto a tassellamento (creato con [**gluNewTess).**](glunewtess.md)

</dd> <dt>

*Che* 
</dt> <dd>

Valore della proprietà da impostare. I valori seguenti sono validi: GLU \_ TESS \_ WINDING \_ RULE, GLU \_ TESS BOUNDARY ONLY e GLU TESS \_ \_ \_ \_ TOLERANCE.



| Valore                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <dt>**REGOLA \_ DI \_ AVVOLGIMENTO GLU \_ TESS**</dt> </dl>    | Determina le parti del poligono all'interno. Il parametro value può essere impostato su uno dei valori seguenti: GLU \_ TESS \_ WINDING \_ ODD, GLU \_ TESS \_ WINDING \_ NONZERO, GLU \_ TESS \_ WINDING \_ POSITIVE, GLU TESS \_ \_ WINDING NEGATIVE o GLU TESS \_ \_ \_ WINDING \_ ABS \_ GEQ \_ TWO. <br/> Per comprendere il funzionamento della regola di avvolgimento, considerare prima di tutto che i contorni di input partizionano il piano in aree. La regola di avvolgimento determina quale di queste aree si trova all'interno del poligono.<br/> Per un singolo contorno C, il numero di avvolgimento di un punto x è semplicemente il numero con segno di rivoluzioni che si effettua intorno a x mentre si viaggia una volta intorno a C (dove in senso antiorario è positivo). Quando sono presenti diversi contorni, i singoli numeri di avvolgimento vengono sommati. Questa procedura associa un valore intero con segno a ogni punto x nel piano. Si noti che il numero di avvolgimento è lo stesso per tutti i punti in una singola area.<br/> La regola di avvolgimento classifica un'area come "all'interno" se il relativo numero di avvolgimento appartiene alla categoria scelta (valore dispari, diverso da zero, positivo, negativo o assoluto di almeno due). Il tessellatore GLU precedente (prima di GLU 1.2) usava la regola "dispari". La regola "diverso da zero" (GLU \_ TESS \_ WINDING NONZERO) è un altro modo comune per \_ definire l'interno. Le altre tre regole (GLU \_ TESS \_ WINDING \_ POSITIVE, GLU \_ TESS \_ WINDING \_ NEGATIVE, GLU TESS \_ \_ WINDING ABS GEQ TWO) \_ \_ \_ sono utili per le operazioni CSG poligonali.<br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <dt>**GLU \_ TESS \_ BOUNDARY \_ ONLY**</dt> </dl> | Specifica un valore booleano (impostare value su GL \_ TRUE o GL \_ FALSE). Quando si imposta value su GL TRUE, viene restituito un set di contorni chiusi che separano l'interno e l'esterno del poligono invece di \_ una facciata. I contorni esterni sono orientati in senso antiorario rispetto alla normale; I contorni interni sono orientati in senso orario. I callback GLU \_ TESS BEGIN e GLU TESS BEGIN DATA usano il tipo GL LINE LOOP \_ per ogni \_ \_ \_ \_ \_ contorno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <dt>**TOLLERANZA \_ GLU TESS \_**</dt> </dl>              | Specifica una tolleranza per l'unione delle funzionalità per ridurre le dimensioni dell'output. Ad esempio, due vertici molto vicini l'uno all'altro potrebbero essere sostituiti da un singolo vertice. La tolleranza viene moltiplicata per la massima grandezza delle coordinate di qualsiasi vertice di input. specifica la distanza massima che qualsiasi funzionalità può spostare come risultato di una singola operazione di unione. Se una singola funzionalità prende parte a diverse operazioni di unione, la distanza totale spostata può essere maggiore. <br/> L'unione delle funzionalità è completamente facoltativa. la tolleranza è solo un suggerimento. L'implementazione è libera di unire in alcuni casi e non in altri o di non unire mai le funzionalità. La tolleranza predefinita è zero.<br/> L'implementazione corrente unisce i vertici solo se sono esattamente coincidenti, indipendentemente dalla tolleranza corrente. Un vertice viene suddiviso in un bordo solo se l'implementazione non è in grado di distinguere il lato del bordo su cui si trova il vertice. Due bordi vengono uniti solo quando entrambi gli endpoint sono identici.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

*value* 
</dt> <dd>

Valore della proprietà indicata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluTessProperty** controlla le proprietà archiviate in un oggetto a tassellamento. Queste proprietà influiscono sul modo in cui i poligoni vengono interpretati e sottoposti a rendering.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**gluGetTessProperty**](glugettessproperty.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> </dl>

 

 





