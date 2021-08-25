---
title: Interfacce di trasferimento dati
description: Interfacce di trasferimento dati
ms.assetid: c42e65a4-7b77-4f39-8323-04fa60c5b140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63bffa72f2e6bd408cbb7f19121aeef991e74702ff1141b24aba779e6985585c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896341"
---
# <a name="data-transfer-interfaces"></a>Interfacce di trasferimento dati

[**L'interfaccia IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) fornisce ai consumer di dati metodi per ottenere e impostare i dati di un oggetto, determinare i formati supportati dall'oggetto e registrare e ricevere notifiche quando i dati nell'oggetto cambiano. Quando si ottengono dati, un chiamante può specificare il formato in cui vuole eseguire il rendering dei dati. L'origine dei dati, tuttavia, determina il supporto di archiviazione, restituito in un parametro out fornito dal chiamante.

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) fornisce di per sé tutti gli strumenti necessari per implementare Windows di appunti o di documenti composti nelle applicazioni. Se si vuole supportare anche i trasferimenti di trascinamento della selezione, è necessario implementare le [**interfacce IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) insieme a **IDataObject**.

[**L'interfaccia IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) combinata con le API degli Appunti OLE offre tutte le funzionalità Windows API degli Appunti. Non è in genere necessario usare entrambe le API degli Appunti. I fornitori di dati che supportano i trasferimenti di trascinamento della selezione o i documenti composti OLE devono implementare **l'interfaccia IDataObject.** Se l'applicazione supporta ora solo i trasferimenti degli Appunti, ma si intende aggiungere documenti di trascinamento della selezione o composti nelle versioni successive, è possibile implementare **ora IDataObject** e le API degli Appunti OLE per ridurre al minimo il tempo impiegato per il ricodamento e il debug in un secondo momento. È anche possibile implementare **IDataObject** per usare supporti di trasferimento diversi dalla memoria globale.

La tabella seguente riepiloga quelli da usare, a seconda dei tipi di trasferimento dei dati che si vuole supportare:



| Per supportare                                                                       | Uso                                                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Documenti composti<br/>                                                    | [**Idataobject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Trasferimenti con trascinamento della selezione<br/>                                               | [**IDataObject,**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) [**IDropSource,**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) [**IDropTarget,**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) (o l'equivalente)<br/> |
| Trasferimenti degli Appunti tramite memoria globale in modo esclusivo<br/>                   | [API Appunti](../dataxchg/clipboard.md)<br/>                                                                                                                            |
| Trasferimenti degli Appunti tramite mezzi di scambio diversi dalla memoria globale.<br/>  | [**Idataobject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Trasferisce ora gli Appunti, ma trascina e rilascia documenti o documenti compositi in un secondo momento<br/> | [**IDataObject e**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) le interfacce e la funzione elencate sopra per "Trasferimenti di trascinamento della selezione"<br/>                                                    |



 

Quando un utente avvia un'operazione di trasferimento dei dati, l'applicazione di origine crea un'istanza di [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e tramite di essa rende disponibili i dati in uno o più formati. In un trasferimento degli Appunti, l'applicazione chiama la [**funzione OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) per passare un puntatore a oggetto dati a OLE. **OleSetClipboard offre anche** formati di dati degli Appunti standard per le applicazioni OLE versione 1 e non OLE. In un trasferimento di trascinamento della selezione, l'applicazione chiama invece la [**funzione DoDragDrop.**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)

Sul lato ricevente del trasferimento, la destinazione riceve il puntatore [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) come argomento a una chiamata di [**IDropTarget::D rop**](/windows/desktop/api/OleIdl/nf-oleidl-idroptarget-drop) o chiamando la funzione [**OleSetClipboard,**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) a seconda che il trasferimento sia tramite trascinamento della selezione o gli Appunti. Dopo aver ottenuto questo puntatore, la destinazione chiama [**IDataObject::EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc) per informazioni sui formati disponibili per il recupero e sui tipi di supporti che è possibile ottenere. Con queste informazioni, l'applicazione ricevente richiede i dati con una chiamata a [**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento dati](data-transfer.md)
</dt> </dl>

 

