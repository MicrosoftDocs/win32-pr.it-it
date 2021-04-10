---
title: funzione gluTessProperty (Glu. h)
description: La funzione gluTessProperty imposta la proprietà di un oggetto a mosaico.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- funzione gluTessProperty OpenGL
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
ms.openlocfilehash: bfe21f2961cd4cb1df31a1fdb3f407a71d6e6d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121250"
---
# <a name="glutessproperty-function"></a>gluTessProperty (funzione)

La funzione **gluTessProperty** imposta la proprietà di un oggetto a mosaico.

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

Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).

</dd> <dt>

*che* 
</dt> <dd>

Valore della proprietà da impostare. Sono validi i valori seguenti: \_ regola di Winding di Glu Tess \_ \_ , Glu \_ Tess \_ \_ solo limite e Glu \_ Tess \_ tolerance.



| Valore                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <dt>**\_regola di \_ Winding di Glu Tess \_**</dt> </dl>    | Determina quali parti del poligono sono all'interno. Il parametro value può essere impostato su uno dei seguenti elementi: GLU \_ Tess \_ Winding \_ dispari, Glu \_ Tess \_ Winding \_ diverso da zero, GLU \_ Tess \_ Winding \_ positivo, Glu \_ Tess \_ Winding \_ negativo o Glu \_ Tess \_ Winding \_ ABS \_ GEQ \_ Two. <br/> Per comprendere il funzionamento della regola di avvolgimento, considerare prima di tutto che i contorni di input partizionano il piano in aree. La regola di chiusura determina quali di queste aree sono all'interno del poligono.<br/> Per un C a contorno singolo, il numero di serie di un punto x è semplicemente il numero con segno di rivoluzioni che vengono apportate intorno a x mentre si sposta una volta attorno al linguaggio C (in senso antiorario è positivo). Quando sono presenti diversi contorni, i singoli numeri di avvolgimento vengono sommati. Questa procedura associa un valore intero con segno a ogni punto x del piano. Si noti che il numero di avvolgimento è lo stesso per tutti i punti in una singola area.<br/> La regola di avvolgimento classifica un'area come "interna" Se il numero di avvolgimento appartiene alla categoria scelta (dispari, diverso da zero, positivo, negativo o valore assoluto di almeno due). La regola mosaico precedente (precedente a GLU 1,2) usava la regola "dispari". La regola "diverso da zero" (GLU \_ Tess \_ Winding \_ diverso da zero) è un altro modo comune per definire la parte interna. Le altre tre regole (GLU \_ Tess \_ Winding \_ positivo, Glu \_ Tess \_ Winding \_ negative, Glu \_ Tess \_ Winding \_ ABS \_ GEQ \_ Two) sono utili per le operazioni di gestione dei poligoni.<br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <dt>**\_ \_ solo limite del \_ solo Glu Tess**</dt> </dl> | Specifica un valore booleano (impostare valore su GL \_ true o GL \_ false). Quando si imposta Value su GL \_ true, viene restituito un set di contorni chiusi che separa l'interno e l'esterno del poligono anziché uno a mosaico. I contorni esterni sono orientati in senso antiorario rispetto alla normale; i contorni interni sono orientati in senso orario. \_ \_ \_ \_ Per ogni contorno i callback dei dati Begin Tess Begin e Glu Tess Begin \_ data usano il tipo \_ di riga GL \_ .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <dt>**\_tolleranza Glu Tess \_**</dt> </dl>              | Specifica una tolleranza per l'Unione delle funzionalità per ridurre le dimensioni dell'output. Ad esempio, due vertici che sono molto vicini tra loro possono essere sostituiti da un singolo vertice. La tolleranza viene moltiplicata per la grandezza della coordinata più grande di qualsiasi vertice di input; Specifica la distanza massima che qualsiasi funzionalità può spostare come risultato di una singola operazione di merge. Se una singola funzionalità partecipa a diverse operazioni di Unione, la distanza totale spostata può essere maggiore. <br/> L'Unione delle funzionalità è completamente facoltativa. la tolleranza è solo un suggerimento. È possibile eseguire il merge dell'implementazione in alcuni casi, non in altri, oppure non unire mai le funzionalità. La tolleranza predefinita è zero.<br/> L'implementazione corrente unisce i vertici solo se sono esattamente coincidenti, indipendentemente dalla tolleranza corrente. Un vertice viene inserito in un bordo solo se l'implementazione non è in grado di distinguere il lato del bordo su cui si trova il vertice. Due bordi vengono uniti solo quando entrambi gli endpoint sono identici.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

*value* 
</dt> <dd>

Valore della proprietà indicata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluTessProperty** controlla le proprietà archiviate in un oggetto a mosaico. Queste proprietà influiscono sul modo in cui i poligoni vengono interpretati e sottoposti a rendering.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**gluGetTessProperty**](glugettessproperty.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> </dl>

 

 





