---
description: Errori dei componenti in coda
ms.assetid: 29a1bf52-7252-4f8a-bdb7-61b152fb907e
title: Errori dei componenti in coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422ea9c7ff77f2d69633d6db8b8d48c63fabc071
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305010"
---
# <a name="queued-components-errors"></a>Errori dei componenti in coda

Quando una chiamata a un componente in coda ha esito negativo, perché non è stato possibile trasmettere al server (un errore sul lato client) o perché l'esecuzione non è riuscita al momento dell'arrivo (errore sul lato server), il messaggio di [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) corrispondente viene chiamato *messaggio non elaborabile*.

Il servizio componenti in coda COM+ gestisce i messaggi non elaborabili utilizzando una serie di code di tentativi. Dopo diversi tentativi, il messaggio viene spostato in una coda di riposo finale. I messaggi rimangono nella coda di riposo fino a quando non vengono spostati manualmente tramite l'utilità di spostamento messaggi dei componenti in coda. Per ulteriori informazioni sull'utilizzo di Message Mover, vedere [gestione degli errori](handling-errors-in-queued-components.md).

Descrizioni dettagliate della sequenza di eventi che si verificano per diversi tipi di errori sono disponibili negli argomenti descritti nella tabella seguente.



| Argomento                                                                             | Descrizione                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Errori sul lato server](server-side-errors.md)<br/>                           | Viene descritta in dettaglio la risposta del servizio componenti in coda COM+ a un errore sul lato server.<br/>             |
| [Errori lato client](client-side-errors.md)<br/>                           | Viene descritta in dettaglio la risposta del servizio componenti in coda COM+ a un errore sul lato client.<br/>             |
| [Errori persistenti Client-Side](persistent-client-side-failures.md)<br/> | Viene descritto in dettaglio la risposta del servizio componenti in coda COM+ a errori ripetuti sul lato client.<br/> |



 

 

 




