---
description: Rappresenta la possibilità di analizzare il layout di una raccolta di tratti e dividerli in testo e grafica.
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: Classe InkDivider (Msinkaut15.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDivider
- InkDivider.IInkDivider
api_type:
- COM
api_location:
- Inkdiv.dll
- Inkdiv.dll.dll
ms.openlocfilehash: d7dd98aaef627bac6a26340464c14c4e46c07d6a23f32c2664651503b5d79014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220832"
---
# <a name="inkdivider-class"></a>Classe InkDivider

Rappresenta la possibilità di analizzare il layout di una raccolta di tratti e dividerli in testo e grafica.

**InkDivider** ha questi tipi di membri:

-   [Interfacce](#interfaces)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="interfaces"></a>Interfacce

La **classe InkDivider** definisce queste interfacce.



| Interfaccia       | Descrizione                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkDivider** | Questo oggetto implementa **l'interfaccia COM IInkDivider.**<br/> |



 

### <a name="methods"></a>Metodi

La **classe InkDivider** include questi metodi.



| Metodo                              | Descrizione                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dividere**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | Restituisce un [**oggetto IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) che contiene informazioni strutturali sui tratti nell'oggetto **InkDivider.**<br/> |



 

### <a name="properties"></a>Proprietà

La **classe InkDivider** ha queste proprietà.



| Proprietà                                                             | Tipo di accesso           | Descrizione                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta l'altezza prevista della grafia in unità HIMETRIC.<br/>                                                      |
| [**Recognizercontext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta [**l'oggetto InkRecognizerContext usato**](inkrecognizercontext-class.md) per il riconoscimento della grafia.<br/> |
| [**Tratti**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta la [**raccolta InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenuta nell'oggetto **InkDivider.** <br/>     |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il [**metodo CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

**L'oggetto InkDivider** usa il layout dei tratti, l'ordine in cui vengono aggiunti i tratti, la direzione in cui vengono disegnati i tratti e altri fattori per eseguire l'analisi dell'input penna. La [raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) analizzata **dall'oggetto InkDivider** è contenuta nella proprietà [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) dell'oggetto **InkDivider.** **L'oggetto InkDivider** analizza dinamicamente la raccolta InkStrokes durante l'aggiunta o l'eliminazione dalla raccolta, ma non esegue alcuna modifica dei tratti.

I risultati dell'analisi vengono restituiti in [**un oggetto IInkDivisionResult.**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)

**L'oggetto InkDivider** usa un [**oggetto InkRecognizerContext**](inkrecognizercontext-class.md) per dividere i tratti in modo più accurato e per assegnare una stringa di riconoscimento ai risultati.

> [!Note]  
> **L'oggetto InkDivider** usa le impostazioni delle proprietà predefinite dell'oggetto [**InkRecognizerContext.**](inkrecognizercontext-class.md)

 

Se non si assegna un contesto di riconoscimento all'oggetto **InkDivider,** l'oggetto **InkDivider** analizza ancora l'input penna, ma divide i tratti in modo meno accurato e non associa il testo ai risultati della divisione.

> [!Note]  
> La [**proprietà RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) deve essere impostata prima di aggiungere tratti alla [**proprietà Strokes.**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) Dopo che i tratti sono stati aggiunti **all'oggetto InkDivider,** la **proprietà RecognizerContext** non può essere modificata.

 

**InkDivider** attualmente non supporta le lingue verticali. Perché **l'oggetto InkDivider** riconosca correttamente queste lingue, l'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) per la lingua deve supportare la funzionalità di input libero e i caratteri devono essere scritti da sinistra a destra.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                               |
| Intestazione<br/>                   | <dl> <dt>Msinkaut15.h (richiede anche Msinkaut15 \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Inkdiv.dll</dt> </dl>                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> <dt>

[Raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

