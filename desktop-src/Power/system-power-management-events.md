---
description: Un evento di risparmio energia del sistema è una modifica dello stato di alimentazione del sistema, della modalità operativa di un dispositivo o del sistema o del valore di un'impostazione di risparmio energia.
ms.assetid: f73b072a-1f69-4e26-9712-dab428edca18
title: Eventi di risparmio energia del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0558dfe0c846c6b48125a382d14f03181d7f18fb2d11deb4783af975e57c4cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032931"
---
# <a name="system-power-management-events"></a>Eventi di risparmio energia del sistema

Un evento di risparmio energia del sistema è una modifica dello stato di alimentazione del sistema, della modalità operativa di un dispositivo o del sistema o del valore di un'impostazione di risparmio energia. Poiché questi eventi possono influire sul funzionamento delle applicazioni e dei driver installabili, il sistema notifica tutte le applicazioni e i driver installabili trasmettendo una notifica per ogni evento. Le applicazioni e i servizi si registrano per le notifiche usando la [**funzione RegisterPowerSettingNotification.**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) Le notifiche vengono ricevute tramite il [**messaggio WM \_ POWERBROADCAST,**](wm-powerbroadcast.md) che contiene l'evento di risparmio energia e tutti i dati specifici dell'evento associati.

## <a name="system-power-status-events"></a>Eventi di stato dell'alimentazione del sistema

Un *evento di stato dell'alimentazione del* sistema si verifica quando viene apportata una modifica all'alimentatore o allo stato della batteria del sistema. Ad esempio, il sistema trasmette un evento [ \_ PBT APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) ogni volta che l'utente passa dalla batteria all'alimentazione CA o viceversa. Il sistema trasmette questo evento anche quando l'autonomia della batteria scende sotto la soglia specificata dall'utente o se lo stato di carica della batteria cambia di una percentuale specificata.

## <a name="operational-mode-events"></a>Eventi in modalità operativa

Un *evento in modalità* operativa si verifica quando si verifica una modifica del consumo di energia, ad esempio quando il sistema passa a uno stato di sospensione a causa di inattività o l'utente mette manualmente il sistema in sospensione. Il sistema trasmette gli eventi relativi a queste modifiche prima che venga apportata la modifica al consumo di energia. Ad esempio, se il sistema determina che è inattivo, trasmette un evento [ \_ PBT APMSUSPEND](pbt-apmsuspend.md) che notifica ad applicazioni e driver che sta per sospendere l'operazione e la sospensione per risparmiare energia. Le applicazioni e i driver possono prepararsi per la sospensione chiudendo i file e salvando i dati per evitare la potenziale perdita di dati.

Quando il sistema esegue una sospensione *critica,* il sistema viene messo in sospensione immediatamente a causa di una condizione critica, ad esempio un allarme batteria critico. A differenza di una normale transizione di sospensione, il sistema non invia notifiche ad applicazioni e driver prima di eseguire una sospensione critica. Pertanto, le applicazioni devono essere preparate per gestire le sospensioni critiche.

Quando il funzionamento del sistema viene ripristinato dopo essere stato sospeso, il sistema invia una notifica a tutte le applicazioni e i driver. Indica anche se il sistema sta riprendendo da una sospensione critica in modo che l'applicazione o il driver possa eseguire i passaggi appropriati per ripristinare i dati e continuare l'operazione.

Le applicazioni devono eseguire ogni tentativo di gestire la transizione allo stato di sospensione senza alcun intervento dell'utente perché potrebbe non essere possibile che l'utente risponda. Ad esempio, il coperchio nel computer notebook potrebbe essere chiuso. Quando un'applicazione riceve una notifica che indica che il sistema sta per passare alla sospensione, deve eseguire rapidamente le operazioni necessarie e tornare al di fuori del ciclo di messaggi. Il sistema consente un massimo di due secondi per ogni applicazione quando si gestisce questo messaggio prima del timeout.

## <a name="power-setting-change-events"></a>Eventi di modifica delle impostazioni di risparmio energia

Un evento di modifica dell'impostazione di risparmio energia si verifica quando viene apportata una modifica al valore di un'impostazione di risparmio energia. Ad esempio, l'utente modifica la combinazione per il risparmio di energia da Prestazioni elevate a Bilanciata nell'applicazione Opzioni risparmio energia in Pannello di controllo. In questo caso, il sistema trasmette un evento che indica che la combinazione per il risparmio di energia è stata modificata. Questo evento include il nuovo valore per l'impostazione di risparmio energia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Risparmio energia](about-power-management.md)
</dt> </dl>

 

 



