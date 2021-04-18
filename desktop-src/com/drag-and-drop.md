---
title: Trascinamento e rilascio
description: Il trascinamento della selezione si riferisce ai trasferimenti di dati in cui un mouse o un altro dispositivo di puntamento viene usato per specificare sia l'origine dati che la relativa destinazione.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc4b425637432024d097acb8afdc5e169467c6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298347"
---
# <a name="drag-and-drop"></a>Trascinamento e rilascio

Il *trascinamento della selezione* si riferisce ai trasferimenti di dati in cui un mouse o un altro dispositivo di puntamento viene usato per specificare sia l'origine dati che la relativa destinazione. In una tipica operazione di trascinamento della selezione, un utente seleziona l'oggetto da trasferire spostando il puntatore del mouse su di esso e tenendo premuto il pulsante sinistro o un altro pulsante designato a questo scopo. Continuando a tenere premuto il pulsante, l'utente avvia il trasferimento trascinando l'oggetto nella relativa destinazione, che può essere qualsiasi contenitore OLE. Il trascinamento della selezione fornisce esattamente la stessa funzionalità degli Appunti OLE copia e incolla, ma aggiunge commenti e suggerimenti visivi ed elimina la necessità di menu. Infatti, se un'applicazione supporta la copia e incolla degli Appunti, per supportare il trascinamento della selezione è necessario molto altro.

Durante un'operazione di trascinamento e rilascio OLE vengono usate le tre parti separate di codice seguenti.



| Origine codice di trascinamento della selezione                               | Implementazione e utilizzo                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaccia [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> | Implementata dall'oggetto che contiene i dati trascinati, a cui viene fatto riferimento come *origine del trascinamento*.<br/>                                                                                         |
| [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) (interfaccia)<br/> | Implementata dall'oggetto che ha lo scopo di accettare l'eliminazione, denominata destinazione di *rilascio*.<br/>                                                                                 |
| [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) (funzione)<br/>    | Implementato da OLE e utilizzato per avviare un'operazione di trascinamento della selezione. Dopo che l'operazione è in corso, facilita la comunicazione tra l'origine di trascinamento e l'obiettivo di rilascio.<br/> |



 

Le interfacce [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) possono essere implementate in un contenitore o in un'applicazione a oggetti. Il ruolo di origine di trascinamento o destinazione di rilascio non è limitato a un tipo di applicazione OLE.

La funzione OLE [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implementa un ciclo che tiene traccia del movimento del mouse e della tastiera fino al momento in cui viene annullato o si verifica un trascinamento. **DoDragDrop** è la funzione chiave nel processo di trascinamento della selezione, che facilita la comunicazione tra l'origine di trascinamento e l'obiettivo di rilascio.

Durante un'operazione di trascinamento della selezione, è possibile visualizzare tre tipi di commenti e suggerimenti all'utente.



| Tipo di feedback            | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Feedback sull'origine<br/>  | Fornito dall'origine di trascinamento, il feedback sull'origine indica che i dati vengono trascinati e non cambiano nel corso del trascinamento. In genere, i dati vengono evidenziati per segnalare che è stata selezionata.<br/>                                                                                                                                            |
| Feedback del puntatore<br/> | Fornito dall'origine di trascinamento, il feedback del puntatore indica cosa accade se il mouse viene rilasciato in un determinato momento. Il feedback del puntatore cambia continuamente quando l'utente sposta il mouse e/o preme un tasto di modifica. Se, ad esempio, il puntatore viene spostato in una finestra che non può accettare un rilascio, il puntatore viene modificato nel simbolo "non consentito".<br/> |
| Feedback di destinazione<br/>  | Fornito dalla destinazione di rilascio, il feedback di destinazione indica dove deve essere eseguito il rilascio.<br/>                                                                                                                                                                                                                                                                    |



 

Per altre informazioni, vedere [trascinare le responsabilità dell'origine](drag-source-responsibilities.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento dati](data-transfer.md)
</dt> </dl>

 

 





