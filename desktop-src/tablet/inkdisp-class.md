---
description: Rappresenta i tratti di input penna raccolti in uno spazio di input penna.
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: Classe InkDisp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 429cbf85bdc92753cda1e58a0e89086b4b5b8b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750210"
---
# <a name="inkdisp-class"></a>Classe InkDisp

Rappresenta i tratti di input penna raccolti in uno spazio di input penna.

**InkDisp** dispone di questi tipi di membri:

-   [Eventi](#events)
-   [Interfacce](#interfaces)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

La classe **InkDisp** presenta questi eventi.



| Event                                    | Descrizione                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | Si verifica quando viene aggiunto un tratto all'oggetto **InkDisp** .<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | Si verifica quando un tratto viene eliminato dall'oggetto **InkDisp** .<br/> |



 

### <a name="interfaces"></a>Interfacce

La classe **InkDisp** definisce queste interfacce.



| Interfaccia    | Descrizione                                                       |
|:-------------|:------------------------------------------------------------------|
| **IInkDisp** | Questo oggetto implementa l'interfaccia com **IInkDisp** .<br/> |



 

### <a name="methods"></a>Metodi

La classe **InkDisp** dispone di questi metodi.



| Metodo                                                                   | Descrizione                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStrokesAtRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | Inserisce una raccolta di tratti nell'oggetto **InkDisp** in corrispondenza del rettangolo specificato.<br/>                                                                                                       |
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | Indica se [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) può essere convertito in un oggetto **InkDisp** .<br/>                                                                                       |
| [**Clip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | Rimuove parti di un tratto o di una raccolta di tratti esterni a un rettangolo.<br/>                                                                                                       |
| [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | Copia la raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) negli Appunti.<br/>                                                                                                           |
| [**ClipboardCopyWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | Copia gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) contenuti nel rettangolo noto negli Appunti.<br/>                                                               |
| [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | Copia [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) dagli Appunti nell'oggetto **InkDisp** .<br/>                                                                                               |
| [**Clone**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | Crea un oggetto **InkDisp** duplicato.<br/>                                                                                                                                                   |
| [**CreateStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | Crea un tratto da punti o dati di pacchetti.<br/>                                                                                                                                              |
| [**CreateStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | Crea una raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) per questo oggetto **InkDisp** .<br/>                                                                                                |
| [**DeleteStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | Elimina un tratto dall'oggetto **InkDisp** .<br/>                                                                                                                                             |
| [**DeleteStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | Elimina i tratti dall'oggetto **InkDisp** .<br/>                                                                                                                                              |
| [**Metodo ExtractStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | Estrae tratti dall'oggetto **InkDisp** e restituisce un nuovo oggetto **InkDisp** che contiene i tratti estratti.<br/>                                                                       |
| [**Metodo ExtractWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | Taglia o copia i tratti da un oggetto della **classe InkDisp** esistente e li incolla in un nuovo oggetto della **classe InkDisp** , usando il rettangolo noto per determinare i tratti da estrarre.<br/> |
| [**GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | Recupera il rettangolo di delimitazione di tutti i tratti nell'oggetto **InkDisp** .<br/>                                                                                                               |
| [**HitTestCircle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | Recupera la raccolta [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) completamente interna o intersecata da un cerchio noto.<br/>                                                  |
| [**HitTestWithLasso**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | Recupera i tratti all'interno di un'area di selezione della polilinea.<br/>                                                                                                                                   |
| [**HitTestWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | Recupera i tratti contenuti all'interno di un rettangolo specificato.<br/>                                                                                                                    |
| [**Caricamento**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | Compila un nuovo oggetto **InkDisp** con dati binari noti.<br/>                                                                                                                                |
| [**NearestPoint**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | Recupera il [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) all'interno dell'oggetto **InkDisp** più vicino a un punto noto, fornendo facoltativamente informazioni aggiuntive.<br/>                       |
| [**Salva**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | Converte l'input penna in un formato specificato e restituisce i dati binari.<br/>                                                                                                                       |



 

### <a name="properties"></a>Proprietà

La classe **InkDisp** dispone di queste proprietà.



| Proprietà                                                                           | Tipo di accesso           | Descrizione                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | Sola lettura<br/>  | Ottiene la raccolta [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) da salvare in modo permanente con l'input penna.<br/>                             |
| [**Sporco**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | Lettura/Scrittura<br/> | Ottiene o imposta il valore che indica se un oggetto **InkDisp** è stato modificato dall'ultima volta in cui è stato salvato l'input penna.<br/> |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Sola lettura<br/>  | Ottiene la raccolta di dati definiti dall'applicazione.<br/>                                                                             |
| [**Tratti**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | Sola lettura<br/>  | Ottiene la raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenuta nell'oggetto **InkDisp** .<br/>                             |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

> [!Note]  
> La prima istanza di questo oggetto causa anche la creazione di un'istanza di GDI+. Un effetto collaterale è che se si usa un singolo oggetto Ink in un ciclo e lo si crea ed Elimina definitivamente all'interno del ciclo, si causerà la creazione di un'istanza di GDI+. Questo può causare un calo delle prestazioni nell'applicazione. Per evitare questo problema, è possibile lasciare sempre una singola istanza di un oggetto Ink mentre l'applicazione usa l'input penna.

 

Un oggetto **InkDisp** è un contenitore di dati Stroke (Point). I dati del tratto, o i punti raccolti dalla penna, vengono inseriti in un oggetto **InkDisp** . La proprietà [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) contiene i dati per tutti i tratti all'interno dell'oggetto **InkDisp** .

L'oggetto [**InkCollector**](inkcollector-class.md) , l'oggetto [**InkOverlay**](inkoverlay-class.md) e il controllo [InkPicture](inkpicture-control-reference.md) raccoglie i punti dal dispositivo di input e li inserisce in un oggetto **InkDisp** . Questi oggetti agiscono essenzialmente come origine che distribuisce l'input penna in uno o più oggetti **InkDisp** diversi, che fungono da contenitori che contengono l'input penna distribuito.

Lo spazio di input penna è uno spazio delle coordinate virtuali a cui viene eseguito il mapping delle coordinate del contesto della tavoletta. Questo spazio è stato corretto in un sistema di coordinate HIMETRIC. Nelle coordinate dello spazio input penna, uno spostamento da 0 a 1 è uguale a 1 unità HIMETRIC. Questo mapping semplifica la correlazione di più oggetti **InkDisp** .

L'oggetto [**InkRenderer**](inkrenderer-class.md) gestisce i mapping tra l'input penna e la finestra di visualizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Interfaccia IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

