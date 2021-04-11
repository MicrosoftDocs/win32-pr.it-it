---
title: Informazioni su Windows Connect Now
description: Windows Connect Now (WCN) fornisce un meccanismo semplice e sicuro per i dispositivi e i punti di accesso alla rete, ad esempio stampanti, fotocamere e PC, per la connessione e lo scambio delle impostazioni.
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0118c6a053c480a36138f8dae850ee0862501944
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118295"
---
# <a name="about-windows-connect-now"></a>Informazioni su Windows Connect Now

Windows Connect Now (WCN) fornisce un meccanismo semplice e sicuro per i dispositivi e i punti di accesso alla rete, ad esempio stampanti, fotocamere e PC, per la connessione e lo scambio delle impostazioni. Questa API è l'implementazione Microsoft Wi-Fi del protocollo/Wi-Fi Simple Configuration (WSC), che è stato creato da Wi-Fi Alliance come soluzione per la rete domestica e le piccole imprese. Questa tecnologia non è destinata a scenari aziendali.

> [!Note]  
> Il nome della specifica è stato modificato tra la versione 1.0 e la versione 2. La specifica della versione 1.0 è stata denominata Wi-Fi installazione protetta (WPS). A partire dalla specifica della versione 2, la specifica è denominata Wi-Fi Simple Configuration (WSC). Nella documentazione, i termini WPS e WSC vengono usati in modo interscambiabile, a meno che non sia stato specificato.

 

Windows Connect consente ora alle applicazioni di cercare i dispositivi con supporto per WCN usando l' [API di individuazione funzioni](/previous-versions/windows/desktop/fundisc/fd-portal). L'ambito di una ricerca può essere limitato a uno specifico SSID, stato, categoria o persino ampliato per includere tutti i dispositivi che supportano WCN. Una volta individuati i dispositivi, l'API WCN consente la comunicazione con il dispositivo che supporta WCN per semplificare la configurazione o la connettività.

 

 