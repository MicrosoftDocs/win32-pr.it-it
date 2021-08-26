---
description: Il monitoraggio del tono monitora il flusso multimediale di una chiamata per i toni specificati.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Monitoraggio del tono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb811d91a70f439ae17123b35967800914bd6a04f1a30168754f602231f038e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034181"
---
# <a name="tone-monitoring"></a>Monitoraggio del tono

Il monitoraggio del tono monitora il flusso multimediale di una chiamata per i toni specificati. Un tono è descritto dalle frequenze e dalla cadenza dei componenti. Un'implementazione dell'API può consentire il monitoraggio simultaneo di diversi toni diversi. Un'applicazione può contrassegnare ogni tono per poter distinguere i diversi toni per cui richiede il rilevamento.

Un'applicazione può abilitare o disabilitare il monitoraggio del tono in una chiamata specificata [**con lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones). Con questa funzione, l'applicazione indica i toni da rilevare in una chiamata specificata. Quando il monitoraggio del tono è abilitato, le cifre rilevate causano la notifica dell'applicazione con il [**messaggio LINE \_ MONITORTONE.**](line-monitortone.md) Questo messaggio fornisce l'handle di chiamata in cui è stato rilevato il tono, nonché il tag dell'applicazione per il tono.

L'ambito del monitoraggio del tono è associato alla durata della chiamata. Il monitoraggio del tono in una chiamata termina non appena la chiamata *si disconnette* o diventa *inattiva.*

> [!Note]  
> Il monitoraggio di toni, cifre o tipi di supporti spesso richiede l'uso di risorse di cui il provider di servizi può avere solo una quantità finita. Una richiesta di monitoraggio può essere rifiutata se le risorse non sono disponibili. Per lo stesso motivo, un'applicazione deve disabilitare qualsiasi monitoraggio non necessario.

 

 

 



