---
title: Interfacce di Trasferimento dati
description: Interfacce di Trasferimento dati
ms.assetid: c42e65a4-7b77-4f39-8323-04fa60c5b140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448e1a580880c7202ec67d12965f6db7e0be99d0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300512"
---
# <a name="data-transfer-interfaces"></a>Interfacce di Trasferimento dati

L'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) fornisce ai consumer dei dati i metodi per ottenere e impostare i dati di un oggetto, determinare quali formati sono supportati dall'oggetto e registrarsi per ricevere notifiche quando vengono modificati i dati nell'oggetto. Quando si ottengono dati, un chiamante può specificare il formato in cui desidera eseguire il rendering dei dati. L'origine dei dati, tuttavia, determina il supporto di archiviazione, restituito in un parametro out fornito dal chiamante.

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) fornisce tutti gli strumenti necessari per implementare i trasferimenti degli Appunti di Windows o i trasferimenti di documenti compositi nelle applicazioni. Se si vuole anche supportare i trasferimenti di trascinamento della selezione, è necessario implementare le interfacce [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) insieme a **IDataObject**.

L'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) combinata con le API degli Appunti OLE fornisce tutte le funzionalità delle API degli Appunti di Windows. Non è in genere necessario usare entrambe le API degli Appunti. I fornitori di dati che supportano i trasferimenti con trascinamento della selezione o i documenti composti OLE devono implementare l'interfaccia **IDataObject** . Se l'applicazione supporta ora solo i trasferimenti degli Appunti, ma si desidera aggiungere documenti di trascinamento o composti nelle versioni successive, è possibile implementare **IDataObject** e le API degli Appunti OLE per ridurre al minimo la quantità di tempo impiegato per la ricodifica e il debug in un secondo momento. È anche possibile implementare **IDataObject** per poter utilizzare supporti di trasferimento diversi dalla memoria globale.

Nella tabella seguente vengono riepilogate le opzioni da utilizzare, a seconda dei tipi di trasferimento dei dati che si desidera supportare:



| Per supportare                                                                       | Uso                                                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Documenti composti<br/>                                                    | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Trascinamento della selezione<br/>                                               | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource), [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget), [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) (o equivalente)<br/> |
| Trasferimenti degli Appunti utilizzando esclusivamente la memoria globale<br/>                   | [API Appunti](../dataxchg/clipboard.md)<br/>                                                                                                                            |
| Trasferimenti degli Appunti con supporti di Exchange diversi dalla memoria globale.<br/>  | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Il trasferimento degli Appunti è ora, ma è possibile trascinare e rilasciare documenti compositi<br/> | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e le interfacce e la funzione elencate in precedenza per i trasferimenti di trascinamento della selezione<br/>                                                    |



 

Quando un utente avvia un'operazione di trasferimento dei dati, l'applicazione di origine crea un'istanza di [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e tramite essa rende disponibili i dati in uno o più formati. In un trasferimento degli Appunti, l'applicazione chiama la funzione [**OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) per passare un puntatore a un oggetto dati a OLE. (**OleSetClipboard** offre anche formati di dati degli Appunti standard per le applicazioni OLE versione 1 e non OLE). In un trasferimento con trascinamento della selezione, l'applicazione chiama invece la funzione [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) .

Sul lato ricevente del trasferimento, la destinazione riceve il puntatore [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) come argomento di una chiamata di [**IDropTarget::D por**](/windows/desktop/api/OleIdl/nf-oleidl-idroptarget-drop) o chiamando la funzione [**OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) , a seconda che il trasferimento sia mediante trascinamento della selezione o degli Appunti. Se si ottiene questo puntatore, la destinazione chiama [**IDataObject:: EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc) per informazioni sui formati disponibili per il recupero e sui tipi di supporti che è possibile ottenere. Con queste informazioni, l'applicazione ricevente richiede i dati con una chiamata a [**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento dati](data-transfer.md)
</dt> </dl>

 

