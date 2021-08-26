---
title: Sviluppare app UWP (Universal Windows Platform)
description: Sviluppare app UWP (Universal Windows Platform)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 332864b00614ceb494b2832c0b565a5a10819d631ecb6c4098284a94ad2c038e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935441"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a>Sviluppare app UWP (Universal Windows Platform)

Si consiglia a tutti gli ISV di app desktop (Win32) di portare le app desktop alla piattaforma [UWP (Universal Windows Platform)](https://developer.microsoft.com/windows/bridges/desktop/) tramite il Desktop Bridge. Le app UWP sono supportate anche in [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), quindi risulta più semplice fornire agli utenti un aggiornamento di versione coerente, con conseguente riduzione dei costi di supporto.

Se le app desktop non possono essere convertite usando il Desktop Bridge, è consigliabile usare un programma di installazione che segua le procedure consigliate e verificare che sia completamente testato. Un programma di installazione è la prima esperienza dell'utente o del cliente con l'app. Troppo spesso, questi programmi non funzionano correttamente o non vengono testati in modo accurato per tutti gli scenari. Il kit di certificazione app [Windows](https://dev.windows.com/develop/app-certification-kit) consente di testare l'installazione e la disinstallazione dell'app Win32 e di identificare l'uso di API non documentate, nonché altri problemi di base relativi alle procedure consigliate relative alle prestazioni prima che gli utenti eservitino questa operazione.

## <a name="best-practices"></a>Procedure consigliate:

-   Usa programmi di installazione compatibili sia con le versioni a 32 bit che con quelle a 64 bit di Windows.
-   Progetta i programmi di installazione per l'esecuzione in più scenari (livello utente o computer).
-   Mantieni tutti i componenti ridistribuibili Windows nel pacchetto originale. La modifica del pacchetto può causare malfunzionamenti del programma di installazione.
-   Pianifica tempi di sviluppo adeguati per i programmi di installazione. Spesso ne viene sottovalutata l'importanza durante il ciclo di vita di sviluppo del software.

 

 




