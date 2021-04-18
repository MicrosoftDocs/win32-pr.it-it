---
description: Un evento di risparmio energia del sistema è una modifica dello stato di alimentazione del sistema, della modalità operativa di un dispositivo o del sistema o del valore di un'impostazione di risparmio energia.
ms.assetid: f73b072a-1f69-4e26-9712-dab428edca18
title: Eventi di risparmio energia di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab18fad9116cfff9e1cd35703e32a49e3b12c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312015"
---
# <a name="system-power-management-events"></a>Eventi di risparmio energia di sistema

Un evento di risparmio energia del sistema è una modifica dello stato di alimentazione del sistema, della modalità operativa di un dispositivo o del sistema o del valore di un'impostazione di risparmio energia. Poiché questi eventi possono influire sul funzionamento delle applicazioni e dei driver installabili, il sistema invia una notifica a tutte le applicazioni e ai driver installabili tramite la trasmissione di una notifica per ogni evento. Registri applicazioni e servizi per le notifiche tramite la funzione [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) . Le notifiche vengono ricevute tramite il messaggio [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) , che contiene l'evento di risparmio energia e tutti i dati specifici degli eventi associati.

## <a name="system-power-status-events"></a>Eventi di stato dell'alimentazione del sistema

Un *evento di stato di alimentazione del sistema* si verifica quando viene apportata una modifica all'alimentatore o allo stato della batteria del sistema. Ad esempio, il sistema trasmette un evento [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) ogni volta che l'utente passa dalla batteria all'alimentazione CA o viceversa. Il sistema trasmette questo evento anche quando l'autonomia della batteria scende sotto la soglia specificata dall'utente o se lo stato di carica della batteria cambia di una percentuale specificata.

## <a name="operational-mode-events"></a>Eventi in modalità operativa

Un *evento in modalità operativa* si verifica quando viene apportata una modifica al consumo di energia, ad esempio quando il sistema passa a uno stato di sospensione a causa di inattività o se l'utente inserisce manualmente il sistema in sospensione. Il sistema trasmette gli eventi relativi a queste modifiche prima che venga apportata la modifica al consumo di energia elettrica. Se, ad esempio, il sistema determina che è inattivo, trasmette un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) che informa le applicazioni e i driver che sta per sospendere l'operazione e la sospensione per conservare l'energia. Le applicazioni e i driver possono preparare la sospensione chiudendo i file e salvando i dati per evitare una potenziale perdita di dati.

Quando il sistema esegue una *sospensione critica*, il sistema viene immediatamente messo in sospensione a causa di una condizione critica, ad esempio un allarme di batteria critica. A differenza di una normale transizione di sospensione, il sistema non notifica le applicazioni e i driver prima di eseguire una sospensione critica. Pertanto, le applicazioni devono essere preparate per la gestione di sospensioni critiche.

Quando l'operazione di sistema viene ripristinata dopo essere stata sospesa, il sistema invia una notifica a tutte le applicazioni e i driver. Indica inoltre se il sistema riprende da una sospensione critica, in modo che l'applicazione o il driver possa eseguire le operazioni appropriate per ripristinare i dati e continuare l'operazione.

Le applicazioni devono eseguire ogni tentativo di gestire la transizione allo stato di sospensione senza alcun intervento dell'utente perché potrebbe non essere possibile per l'utente rispondere. Ad esempio, il coperchio del computer notebook potrebbe essere chiuso. Quando un'applicazione riceve la notifica che il sistema sta per entrare in stato di sospensione, deve eseguire rapidamente tutte le operazioni necessarie e restituire il ciclo di messaggi. Il sistema consente un massimo di due secondi per applicazione durante la gestione del messaggio prima del timeout.

## <a name="power-setting-change-events"></a>Eventi di modifica delle impostazioni di risparmio energia

Un evento di modifica dell'impostazione di risparmio energia si verifica quando viene apportata una modifica al valore di un'impostazione di risparmio energia. Ad esempio, l'utente modifica la combinazione per il risparmio di energia dalle prestazioni elevate a quelle bilanciate nell'applicazione Opzioni risparmio energia nel pannello di controllo. In questo caso, il sistema trasmette un evento che indica che la combinazione per il risparmio di energia è cambiata. Questo evento include il nuovo valore per l'impostazione di risparmio energia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> </dl>

 

 



