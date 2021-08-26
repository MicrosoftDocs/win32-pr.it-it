---
description: "Classe InkDisp: rappresenta i tratti di input penna raccolti all'interno di uno spazio input penna."
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: Classe InkDisp (Msinkaut.h)
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
ms.openlocfilehash: 928bda8af246b41bab2c285a5292155917ba8903c6dd71c20177dbf906c64924
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939161"
---
# <a name="inkdisp-class"></a>Classe InkDisp

Rappresenta i tratti raccolti dell'input penna all'interno di uno spazio input penna.

**InkDisp** ha questi tipi di membri:

-   [Eventi](#events)
-   [Interfacce](#interfaces)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

La **classe InkDisp** include questi eventi.



| Event                                    | Descrizione                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | Si verifica quando un tratto viene aggiunto **all'oggetto InkDisp.**<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | Si verifica quando un tratto viene eliminato **dall'oggetto InkDisp.**<br/> |



 

### <a name="interfaces"></a>Interfacce

La **classe InkDisp** definisce queste interfacce.



| Interfaccia    | Descrizione                                                       |
|:-------------|:------------------------------------------------------------------|
| **IInkDisp** | Questo oggetto implementa **l'interfaccia COM IInkDisp.**<br/> |



 

### <a name="methods"></a>Metodi

La **classe InkDisp** include questi metodi.



| Metodo                                                                   | Descrizione                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStrokesAtRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | Inserisce una raccolta di tratti **nell'oggetto InkDisp** in corrispondenza del rettangolo specificato.<br/>                                                                                                       |
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | Indica se [**l'oggetto IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) può essere convertito in un **oggetto InkDisp.**<br/>                                                                                       |
| [**Clip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | Rimuove parti di un tratto o di una raccolta di tratti esterni a un rettangolo.<br/>                                                                                                       |
| [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | Copia la [raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) negli Appunti.<br/>                                                                                                           |
| [**ClipboardCopyWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | Copia negli [**Appunti gli oggetti IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) contenuti nel rettangolo noto.<br/>                                                               |
| [**AppuntiPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | Copia [**l'oggetto IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) dagli Appunti all'oggetto **InkDisp.**<br/>                                                                                               |
| [**Clone**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | Crea un oggetto **InkDisp** duplicato.<br/>                                                                                                                                                   |
| [**CreateStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | Crea un tratto dai punti o dai dati del pacchetto.<br/>                                                                                                                                              |
| [**CreateStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | Crea una [raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) per questo **oggetto InkDisp.**<br/>                                                                                                |
| [**Sequenza di eliminazione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | Elimina un tratto **dall'oggetto InkDisp.**<br/>                                                                                                                                             |
| [**Elimina sequenze**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | Elimina i tratti **dall'oggetto InkDisp.**<br/>                                                                                                                                              |
| [**Metodo ExtractStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | Estrae i tratti **dall'oggetto InkDisp** e restituisce un nuovo **oggetto InkDisp** contenente i tratti estratti.<br/>                                                                       |
| [**Metodo ExtractWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | Taglia o copia i tratti da un oggetto **Classe InkDisp** esistente e li incolla in un nuovo oggetto **Classe InkDisp,** usando il rettangolo noto per determinare quali tratti estrarre.<br/> |
| [**GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | Recupera il rettangolo di selezione di tutti i tratti **nell'oggetto InkDisp.**<br/>                                                                                                               |
| [**HitTestCircle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | Recupera la raccolta [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) completamente all'interno o intersecata da un cerchio noto.<br/>                                                  |
| [**HitTestWithLasso**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | Recupera i tratti all'interno di un'area di selezione polilinea.<br/>                                                                                                                                   |
| [**HitTestWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | Recupera i tratti contenuti all'interno di un rettangolo specificato.<br/>                                                                                                                    |
| [**Caricamento**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | Popola un nuovo **oggetto InkDisp** con dati binari noti.<br/>                                                                                                                                |
| [**NearestPoint**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | Recupera [**l'oggetto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) all'interno **dell'oggetto InkDisp** più vicino a un punto noto, fornendo facoltativamente informazioni aggiuntive.<br/>                       |
| [**Salva**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | Converte l'input penna in un formato specificato e restituisce i dati binari.<br/>                                                                                                                       |



 

### <a name="properties"></a>Proprietà

La **classe InkDisp** ha queste proprietà.



| Proprietà                                                                           | Tipo di accesso           | Descrizione                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Sequenze personalizzate**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | Sola lettura<br/>  | Ottiene la [**raccolta IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) da rendere persistente con l'input penna.<br/>                             |
| [**Sporco**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | Lettura/Scrittura<br/> | Ottiene o imposta il valore che indica se un **oggetto InkDisp** è stato modificato dall'ultimo salvataggio dell'input penna.<br/> |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Sola lettura<br/>  | Ottiene la raccolta di dati definiti dall'applicazione.<br/>                                                                             |
| [**Tratti**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | Sola lettura<br/>  | Ottiene la [raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenuta nell'oggetto **InkDisp.**<br/>                             |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il [**metodo CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

> [!Note]  
> La prima creazione di un'istanza di questo oggetto GDI+ viene creata anche un'istanza di . Un effetto collaterale è che se si usa un singolo oggetto input penna in un ciclo e lo si crea ed elimina all'interno del ciclo, si creerà un'istanza di GDI+ più volte. Ciò può causare una riduzione delle prestazioni nell'applicazione. Per evitare questo problema, mantenere sempre una singola istanza di un oggetto input penna mentre l'applicazione usa l'input penna.

 

Un **oggetto InkDisp** è un contenitore di dati del tratto (punto). I dati del tratto, o i punti raccolti dalla penna, vengono inseriti in un **oggetto InkDisp.** La [**proprietà Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) contiene i dati per tutti i tratti all'interno dell'oggetto **InkDisp.**

[**L'oggetto InkCollector,**](inkcollector-class.md) [**l'oggetto InkOverlay**](inkoverlay-class.md) e il controllo [InkPicture](inkpicture-control-reference.md) raccolgono i punti dal dispositivo di input e li inserisce in **un oggetto InkDisp.** Questi oggetti fungono essenzialmente da origine che distribuisce l'input penna in uno o più oggetti **InkDisp** diversi, che fungono da contenitori che contengono l'input penna distribuito.

Lo spazio input penna è uno spazio delle coordinate virtuali a cui vengono mappate le coordinate del contesto della tablet. Questo spazio è fisso in un sistema di coordinate HIMETRIC. Nelle coordinate dello spazio input penna, uno spostamento da 0 a 1 equivale a 1 unità HIMETRIC. Questo mapping semplifica la relazione tra più **oggetti InkDisp.**

[**L'oggetto InkRenderer**](inkrenderer-class.md) gestisce i mapping tra input penna e finestra di visualizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Interfaccia IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

