---
description: Un provider di servizi multimediali (MSP) TAPI 3 consente a un'applicazione di controllare in modo significativo i supporti per un meccanismo di trasporto specifico.
ms.assetid: 2dd1268f-b31a-443b-a36b-05c1570e7a8a
title: Informazioni sul provider di servizi multimediali (MSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ef4d19a2f01c047d5fc2afd4a0323d7908fcac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132154"
---
# <a name="about-the-media-service-provider-msp"></a>Informazioni sul provider di servizi multimediali (MSP)

Un provider di servizi multimediali (MSP) TAPI 3 consente a un'applicazione di controllare in modo significativo i supporti per un meccanismo di trasporto specifico. Un MSP esiste sempre abbinato a un provider di servizi di telefonia (TSP). Proprio come un TSP è un livello di astrazione per il controllo delle chiamate, MSP controlla i supporti senza necessità di codifica specifici del dispositivo. Per un esempio di comunicazione MSP/TSP, vedere [Panoramica del provider di servizi TAPI](./tapi-service-provider-overview.md).

Un MSP Abilita il controllo multimediale attraverso l'uso di interfacce speciali di Terminal, flusso e sottoflusso definite da TAPI. Il diagramma in [informazioni sui controlli Call e media](about-call-and-media-controls.md) illustra il modo in cui queste interfacce vengono visualizzate in un'applicazione TAPI 3.

Inoltre, un MSP può implementare interfacce private [specifiche del provider](provider-specific-interfaces.md), che TAPI si aggregano sugli oggetti standard esposti a un'applicazione. Ad esempio, Microsoft IPConf MSP, installato con Microsoft Windows 2000, implementa l'interfaccia [**ITParticipant**](itparticipant.md) , che fornisce i controlli per i singoli membri di una conferenza.

Nell'argomento seguente viene brevemente descritto il MSPs che può essere installato con un sistema operativo Microsoft. Per informazioni dettagliate sulla configurazione e sull'utilizzo, vedere Resource Kit per la piattaforma di destinazione.

È possibile scrivere altri provider di servizi multimediali di terze parti per i protocolli specifici o per i dispositivi fisici. [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md) descrive le interfacce che devono essere implementate per consentire a un MSP di interagire con i componenti della telefonia Microsoft.

 

 
