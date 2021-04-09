---
description: Il monitoraggio dei toni monitora il flusso multimediale di una chiamata per i toni specificati.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Monitoraggio del tono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a3275e5207999896792ee04dc1842b01f4ad0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050128"
---
# <a name="tone-monitoring"></a>Monitoraggio del tono

Il monitoraggio dei toni monitora il flusso multimediale di una chiamata per i toni specificati. Un tono è descritto dalle frequenze e dalla cadenza dei componenti. Un'implementazione dell'API può consentire il monitoraggio simultaneo di diversi colori. Un'applicazione può contrassegnare ogni tono per poter distinguere i diversi toni per i quali richiede il rilevamento.

Un'applicazione può abilitare o disabilitare il monitoraggio dei toni per una chiamata specificata con [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones). Con questa funzione, l'applicazione indica quali toni rilevare in una chiamata specificata. Quando il monitoraggio dei toni è abilitato, le cifre rilevate fanno sì che l'applicazione riceva una notifica con il messaggio di [**riga \_ MONITORTONE**](line-monitortone.md) . Questo messaggio fornisce l'handle di chiamata su cui è stato rilevato il tono e il tag dell'applicazione per il tono.

L'ambito del monitoraggio del tono è associato alla durata della chiamata. Il monitoraggio dei toni in una chiamata termina non appena la chiamata si *disconnette* o diventa *inattiva*.

> [!Note]  
> Il monitoraggio di toni, cifre o tipi di supporti spesso richiede l'uso di risorse di cui il provider di servizi può avere solo un importo finito. Una richiesta di monitoraggio può essere rifiutata se le risorse non sono disponibili. Per lo stesso motivo, un'applicazione deve disabilitare eventuali monitoraggi superflui.

 

 

 



