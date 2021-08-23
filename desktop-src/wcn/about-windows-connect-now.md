---
title: Informazioni Windows Connect Now
description: Windows Connect Now (WCN) fornisce un meccanismo semplice e sicuro per connettere e scambiare le impostazioni dei punti di accesso di rete e dei dispositivi (ad esempio stampanti, fotocamera e PC).
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c46e0acbf2d2eb728b0b62610040aaa08e06d466c5bbd5ab47237c46a8612ddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593711"
---
# <a name="about-windows-connect-now"></a>Informazioni Windows Connect Now

Windows Connect Now (WCN) fornisce un meccanismo semplice e sicuro per connettere e scambiare le impostazioni dei punti di accesso di rete e dei dispositivi (ad esempio stampanti, fotocamera e PC). Questa API è l'implementazione Microsoft del protocollo WSC (Protected Setup)/Wi-Fi Simple Configuration (WSC) di Wi-Fi Protected Setup, creato da Wi-Fi Alliance come soluzione per la rete domestica e le piccole aziende. Questa tecnologia non è destinata agli scenari aziendali.

> [!Note]  
> Il nome della specifica è stato modificato tra la versione 1.0h e la versione 2. La specifica della versione 1.0h è stata denominata Wi-Fi Protected Setup (WPS). A partire dalla versione 2, la specifica è denominata Wi-Fi Simple Configuration (WSC). Nella documentazione i termini WPS e WSC vengono usati in modo intercambiabile, a meno che non venga specificato.

 

Windows Connect Now consente alle applicazioni di cercare dispositivi con supporto WCN usando [l'API di individuazione delle funzioni](/previous-versions/windows/desktop/fundisc/fd-portal). L'ambito di una ricerca può essere ristretto a uno specifico SSID, stato, categoria o persino ampliato per includere tutti i dispositivi con funzionalità WCN. Dopo aver individuato i dispositivi, l'API WCN consente la comunicazione con il dispositivo con funzionalità WCN per facilitare la configurazione o la connettività.

 

 