---
description: I servizi di linea estesa (o i servizi linea specifici del dispositivo) includono tutte le estensioni definite dal provider di servizi per l'API.
ms.assetid: 0f01509e-caa5-4f79-be78-36bd5f23c5d7
title: Funzioni di linea estese
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3531a63357276e6b2ea37365b5d5078d5c1de324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526316"
---
# <a name="extended-line-functions"></a>Funzioni di linea estese

I servizi di linea estesa (o i servizi linea specifici del dispositivo) includono tutte le estensioni definite dal provider di servizi per l'API. L'API definisce un meccanismo che consente ai fornitori del provider di servizi di estendere TAPI usando estensioni specifiche del dispositivo. L'API definisce solo il meccanismo di estensione e, in questo modo, fornisce l'accesso alle estensioni specifiche del dispositivo, ma l'API non ne definisce il comportamento. Il comportamento è completamente definito dal provider di servizi.

TAPI è costituito da definizioni di costanti di flag di bit e scalari, strutture di dati, funzioni e messaggi. Sono definite procedure che consentono a un fornitore di estendere la maggior parte di queste come indicato di seguito.

Per le costanti di dati scalari estendibili, un fornitore del provider di servizi può definire nuovi valori in un intervallo specificato. Poiché la maggior parte delle costanti di dati è **DWORD** s, in genere l'intervallo 0x00000000 tramite 0x7FFFFFFF è riservato per le estensioni future comuni, mentre 0X80000000 tramite 0xFFFFFFFF sono disponibili per le estensioni specifiche del fornitore. Si presuppone che un fornitore definisca i valori che sono estensioni naturali dei tipi di dati definiti dall'API.

Per le costanti di dati dei flag di bit estendibili, un fornitore del provider di servizi può definire nuovi valori per i bit specificati. Poiché la maggior parte delle costanti dei flag di bit sono **DWORD** s, in genere un numero specifico di bit inferiori è riservato per le estensioni comuni, mentre i bit superiori rimanenti sono disponibili per le estensioni specifiche del fornitore. I flag di bit comuni sono assegnati da zero bit. le estensioni specifiche del fornitore devono essere assegnate dal bit 31 verso il basso. Ciò garantisce la massima flessibilità nell'assegnazione di posizioni di bit a estensioni comuni rispetto alle estensioni specifiche del fornitore. Si prevede che un fornitore definisca nuovi valori che sono estensioni naturali dei flag di bit definiti dall'API.

Le strutture di dati estendibili hanno un campo di dimensioni sempre più riservato per l'uso specifico del dispositivo. Con la stessa dimensione, il provider di servizi decide la quantità di informazioni e l'interpretazione. Si prevede che un fornitore che definisce un campo specifico del dispositivo renda le estensioni naturali della struttura di dati originale definita dall'API.

Due funzioni, [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) e [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature), e due messaggi correlati, [**line \_ DEVSPECIFIC**](line-devspecific.md) e [**line \_ DEVSPECIFICFEATURE**](line-devspecificfeature.md), forniscono un meccanismo di estensione specifico del fornitore. La funzione **lineDevSpecific** e il \_ messaggio di riga associato DEVSPECIFIC consentono a un'applicazione di accedere a funzionalità di riga, indirizzo o chiamata specifiche del dispositivo non disponibili con i servizi di telefonia di base o supplementari. Il profilo del parametro della funzione **lineDevSpecific** è generico in quanto la minima interpretazione dei parametri viene eseguita dall'API. L'interpretazione dei parametri è definita dal provider di servizi e deve essere riconosciuta da un'applicazione che li utilizza. I parametri vengono semplicemente passati tramite TAPI dall'applicazione al provider di servizi. Un'applicazione che si basa su estensioni specifiche del dispositivo non funziona in genere con altri provider di servizi; Tuttavia, le applicazioni scritte nei servizi di telefonia di base e supplementare funzioneranno con il provider di servizi esteso.

Per praticità, viene fornita anche una funzione di escape più specializzata. È simile a [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific), ma inserisce l'interpretazione su alcuni parametri. Questa funzione più specializzata è [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature), una funzione di escape specifica del dispositivo per consentire l'invio di funzionalità switch al Commuter. La riga del messaggio [**\_ DEVSPECIFICFEATURE**](line-devspecificfeature.md) è il messaggio specifico del dispositivo inviato all'applicazione come indicazione delle funzionalità inviate al Commuter. Questa funzione e il messaggio associato consentono a un'applicazione di emulare il pulsante premendo il telefono della funzione della riga. Poiché i telefoni delle funzionalità e i significati dei pulsanti sono specifici del fornitore, la chiamata di funzionalità con [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) è anche specifica del fornitore.

Come indicato in precedenza, non esiste alcun registro centrale per gli identificatori del produttore. Viene invece reso disponibile un generatore identificatore univoco (EXTIDGEN).

 

 



