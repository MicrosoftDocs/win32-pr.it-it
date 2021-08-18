---
title: Trascinamento e rilascio
description: Il trascinamento della selezione si riferisce ai trasferimenti di dati in cui viene usato un mouse o un altro dispositivo di puntamento per specificare sia l'origine dati che la relativa destinazione.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b388fc6c051fa73c72720d1f349cd50a4fa6902b8f880fbf5ccfb4cf263a4227
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993161"
---
# <a name="drag-and-drop"></a>Trascinamento e rilascio

*Il trascinamento della* selezione si riferisce ai trasferimenti di dati in cui un mouse o un altro dispositivo di puntamento viene usato per specificare sia l'origine dati che la relativa destinazione. In una tipica operazione di trascinamento della selezione, un utente seleziona l'oggetto da trasferire spostando il puntatore del mouse su di esso e tenendo premuto il pulsante sinistro o un altro pulsante designato a questo scopo. Mentre continua a tenere premuto il pulsante, l'utente avvia il trasferimento trascinando l'oggetto nella destinazione, che può essere qualsiasi contenitore OLE. Il trascinamento della selezione offre esattamente le stesse funzionalità della copia e incolla degli Appunti OLE, ma aggiunge feedback visivo ed elimina la necessità di menu. In realtà, se un'applicazione supporta la copia e incolla degli Appunti, è necessario aggiungere poco per supportare il trascinamento della selezione.

Durante un'operazione di trascinamento della selezione OLE, vengono usate le tre parti di codice separate seguenti.



| Origine del codice di trascinamento della selezione                               | Implementazione e uso                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaccia IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> | Implementato dall'oggetto contenente i dati trascinati, definiti origine *del trascinamento.*<br/>                                                                                         |
| [**Interfaccia IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> | Implementato dall'oggetto che deve accettare l'eliminazione, detto *destinazione di rilascio*.<br/>                                                                                 |
| [**Funzione DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)<br/>    | Implementato da OLE e usato per avviare un'operazione di trascinamento della selezione. Dopo che l'operazione è in corso, facilita la comunicazione tra l'origine di trascinamento e la destinazione di rilascio.<br/> |



 

Le [**interfacce IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) possono essere implementate in un contenitore o in un'applicazione per oggetti. Il ruolo dell'origine di trascinamento o della destinazione di rilascio non è limitato a un tipo di applicazione OLE.

La funzione OLE [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implementa un ciclo che tiene traccia dello spostamento di mouse e tastiera fino a quando il trascinamento non viene annullato o non si verifica un rilascio. **DoDragDrop è** la funzione chiave nel processo di trascinamento della selezione, facilitando la comunicazione tra l'origine del trascinamento e la destinazione di rilascio.

Durante un'operazione di trascinamento della selezione, è possibile visualizzare tre tipi di feedback per l'utente.



| Tipo di feedback            | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Commenti e suggerimenti sull'origine<br/>  | Fornito dall'origine di trascinamento, il feedback dell'origine indica che i dati vengono trascinati e non cambiano durante il trascinamento. In genere, i dati vengono evidenziati per segnalare che sono stati selezionati.<br/>                                                                                                                                            |
| Feedback del puntatore<br/> | Fornito dall'origine di trascinamento, il feedback del puntatore indica cosa accade se il mouse viene rilasciato in un determinato momento. Il feedback del puntatore cambia continuamente quando l'utente sposta il mouse e/o preme un tasto di modifica. Ad esempio, se il puntatore viene spostato in una finestra che non può accettare un rilascio, il puntatore passa al simbolo "non consentito".<br/> |
| Inviare commenti e suggerimenti<br/>  | Fornito dalla destinazione di rilascio, il feedback sulla destinazione indica dove deve verificarsi il rilascio.<br/>                                                                                                                                                                                                                                                                    |



 

Per altre informazioni, vedere [Trascinare le responsabilità dell'origine.](drag-source-responsibilities.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento dati](data-transfer.md)
</dt> </dl>

 

 





