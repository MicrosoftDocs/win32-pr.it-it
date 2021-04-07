---
description: Sviluppo di componenti in coda
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: Sviluppo di componenti in coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748042"
---
# <a name="developing-queued-components"></a>Sviluppo di componenti in coda

Il servizio COM+ Queued Components richiede che tutti i metodi dell'applicazione contengano solo \[ \] parametri in, senza valori restituiti. Poiché l'oggetto server non è necessariamente disponibile quando il client effettua la chiamata, i risultati del server possono essere restituiti inviando un messaggio per la creazione di un altro oggetto. In questo modo, la comunicazione bidirezionale non si verifica in ogni caso, ma solo quando è necessaria, da una serie di messaggi unidirezionali tra oggetti.

Per utilizzare il servizio componenti accodati COM+, è necessario che il servizio [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) sia già installato. Accodamento messaggi non viene installato automaticamente. È necessario selezionare Accodamento messaggi durante l'installazione del sistema operativo oppure utilizzando installazione **applicazioni**. Un certificato interno di Accodamento messaggi viene creato automaticamente all'accesso.

Gli argomenti descritti nella tabella seguente forniscono considerazioni aggiuntive per situazioni più specializzate.



| Argomento                                                                                           | Descrizione                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Passaggio di oggetti come parametro](passing-objects-as-parameters.md)s<br/>                   | Viene descritto come passare gli oggetti \[ come \] parametri nei componenti in coda.<br/>                    |
| [Limitazioni di sicurezza in modalità gruppo di lavoro](security-limitations-in-workgroup-mode.md)<br/> | Vengono descritte le limitazioni relative all'utilizzo dell'autenticazione di Accodamento messaggi in modalità gruppo di lavoro.<br/>       |
| [Considerazioni sul threading](threading-considerations.md)<br/>                             | Vengono descritti i problemi specifici relativi al passaggio di puntatori dell'interfaccia del registratore tra thread.<br/> |
| [Ricezione di una risposta](receiving-a-response.md)<br/>                                     | Viene descritto come creare una risposta a una chiamata a un componente in coda.<br/>                           |



 

 

 




