---
description: I servizi di linea estesi (o servizi di linea specifici del dispositivo) includono tutte le estensioni definite dal provider di servizi all'API.
ms.assetid: 0f01509e-caa5-4f79-be78-36bd5f23c5d7
title: Funzioni di linea estese
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394ad011a5752a45f82de4934a3f87c9f1590870b245fdc113f57badb4298290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003659"
---
# <a name="extended-line-functions"></a>Funzioni di linea estese

I servizi di linea estesi (o servizi di linea specifici del dispositivo) includono tutte le estensioni definite dal provider di servizi all'API. L'API definisce un meccanismo che consente ai fornitori di provider di servizi di estendere TAPI usando estensioni specifiche del dispositivo. L'API definisce solo il meccanismo di estensione e in questo modo fornisce l'accesso alle estensioni specifiche del dispositivo, ma l'API non ne definisce il comportamento. Il comportamento è completamente definito dal provider di servizi.

TAPI è costituito da definizioni di costanti scalari e bit-flag, strutture di dati, funzioni e messaggi. Vengono definite procedure che consentono a un fornitore di estenderne la maggior parte come indicato di seguito.

Per le costanti di dati scalari estensibili, un fornitore di provider di servizi può definire nuovi valori in un intervallo specificato. Poiché la maggior parte delle costanti di dati sono **DWORD,** in genere l'intervallo da 0x00000000 a 0x7FFFFFFF è riservato alle estensioni future comuni, mentre i 0x80000000 tramite 0xFFFFFFFF sono disponibili per estensioni specifiche del fornitore. Il presupposto è che un fornitore definirebbe valori che sono estensioni naturali dei tipi di dati definiti dall'API.

Per le costanti di dati con flag di bit estendibile, un fornitore di provider di servizi può definire nuovi valori per i bit specificati. Poiché la maggior parte delle costanti del flag di bit sono **DWORD,** in genere un numero specifico di bit inferiori è riservato alle estensioni comuni, mentre i restanti bit superiori sono disponibili per le estensioni specifiche del fornitore. I flag di bit comuni vengono assegnati a partire dal bit zero; Le estensioni specifiche del fornitore devono essere assegnate dal bit 31 in giù. Ciò offre la massima flessibilità nell'assegnazione di posizioni di bit alle estensioni comuni rispetto alle estensioni specifiche del fornitore. Un fornitore deve definire nuovi valori che sono estensioni naturali dei flag di bit definiti dall'API.

Le strutture di dati estendibili hanno un campo di dimensioni variabili riservato per l'uso specifico del dispositivo. Con dimensioni variabili, il provider di servizi decide la quantità di informazioni e l'interpretazione. Un fornitore che definisce un campo specifico del dispositivo deve eseguire queste estensioni naturali della struttura di dati originale definita dall'API.

Due funzioni, [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) e [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature), e due messaggi correlati, [**LINE \_ DEVSPECIFIC**](line-devspecific.md) e [**LINE \_ DEVSPECIFICFEATURE**](line-devspecificfeature.md), forniscono un meccanismo di estensione specifico del fornitore. La **funzione lineDevSpecific** e il messaggio LINE DEVSPECIFIC associato consentono a un'applicazione di accedere alle funzionalità di linea, indirizzo o chiamata specifiche del dispositivo che non sono disponibili con i servizi di telefonia basic o \_ supplementare. Il profilo dei parametri della **funzione lineDevSpecific** è generico in questa piccola interpretazione dei parametri effettuata dall'API. L'interpretazione dei parametri è definita dal provider di servizi e deve essere compresa da un'applicazione che li usa. I parametri vengono semplicemente passati tramite TAPI dall'applicazione al provider di servizi. Un'applicazione basata su estensioni specifiche del dispositivo non funzionerà in genere con altri provider di servizi. Tuttavia, le applicazioni scritte nei servizi Basic e Telefonia supplementare funzionano con il provider di servizi esteso.

Per praticità, viene fornita anche una funzione di escape più specializzata. È simile a [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific), ma inserisce l'interpretazione in alcuni parametri. Questa funzione più specializzata è [**lineDevSpecificFeature,**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)una funzione di escape specifica del dispositivo per consentire l'invio di funzionalità di commutazione al commutatore. Il messaggio [**LINE \_ DEVSPECIFICFEATURE è**](line-devspecificfeature.md) il messaggio specifico del dispositivo inviato all'applicazione come indicazione delle funzionalità inviate al commutatore. Questa funzione e il messaggio associato consentono a un'applicazione di emulare le pressione dei pulsanti nel telefono della funzionalità della linea. Poiché i telefoni con funzionalità e i significati dei pulsanti sono specifici del fornitore, anche la chiamata di funzionalità tramite [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) è specifica del fornitore.

Come accennato in precedenza, non esiste alcun registro centrale per gli identificatori del produttore. Viene invece reso disponibile un generatore di identificatori univoci (EXTIDGEN).

 

 



