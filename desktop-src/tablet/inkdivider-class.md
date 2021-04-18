---
description: Rappresenta la possibilità di analizzare il layout di una raccolta di tratti e di suddividerli in testo e grafica.
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: Classe InkDivider (Msinkaut15. h)
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
ms.openlocfilehash: c0658504303968803bd2abff063694701d121390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316852"
---
# <a name="inkdivider-class"></a>Classe InkDivider

Rappresenta la possibilità di analizzare il layout di una raccolta di tratti e di suddividerli in testo e grafica.

**InkDivider** dispone di questi tipi di membri:

-   [Interfacce](#interfaces)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="interfaces"></a>Interfacce

La classe **InkDivider** definisce queste interfacce.



| Interfaccia       | Descrizione                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkDivider** | Questo oggetto implementa l'interfaccia com **IInkDivider** .<br/> |



 

### <a name="methods"></a>Metodi

La classe **InkDivider** dispone di questi metodi.



| Metodo                              | Descrizione                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dividere**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | Restituisce un oggetto [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) che contiene informazioni strutturali sui tratti nell'oggetto **InkDivider** .<br/> |



 

### <a name="properties"></a>Proprietà

La classe **InkDivider** dispone di queste proprietà.



| Proprietà                                                             | Tipo di accesso           | Descrizione                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta l'altezza della grafia prevista in unità HIMETRIC.<br/>                                                      |
| [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta l'oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) utilizzato per il riconoscimento della grafia.<br/> |
| [**Tratti**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta la raccolta [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenuta dall'oggetto **InkDivider** . <br/>     |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

L'oggetto **InkDivider** usa il layout dei tratti, l'ordine in cui vengono aggiunti i tratti, la direzione in cui vengono disegnati i tratti e altri fattori per eseguire l'analisi dell'input penna. La raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) analizzata dall'oggetto **InkDivider** è contenuta nella proprietà [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) dell'oggetto **InkDivider** . L'oggetto **InkDivider** analizza dinamicamente la raccolta InkStrokes quando si aggiunge o si elimina dalla raccolta, ma non esegue alcuna modifica dei tratti.

I risultati dell'analisi vengono restituiti in un oggetto [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .

L'oggetto **InkDivider** usa un oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) per dividere più accuratamente i tratti e per assegnare una stringa di riconoscimento ai risultati.

> [!Note]  
> L'oggetto **InkDivider** utilizza le impostazioni predefinite delle proprietà dell'oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) .

 

Se non si assegna un contesto di riconoscimento all'oggetto **InkDivider** , l'oggetto **InkDivider** analizza ancora l'input penna, ma divide i tratti in modo meno accurato e non associa il testo ai risultati della divisione.

> [!Note]  
> Prima di aggiungere tratti alla proprietà [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) , è necessario impostare la proprietà [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) . Una volta aggiunti i tratti all'oggetto **InkDivider** , non è possibile modificare la proprietà **RecognizerContext** .

 

Il **InkDivider** non supporta attualmente le lingue verticali. Affinché l'oggetto **InkDivider** riconosca tali lingue in modo appropriato, l'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) per la lingua deve supportare la funzionalità di input libero e i caratteri devono essere scritti da sinistra a destra.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                               |
| Intestazione<br/>                   | <dl> <dt>Msinkaut15. h (richiede anche Msinkaut15 \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Inkdiv.dll</dt> </dl>                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> <dt>

[Raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

