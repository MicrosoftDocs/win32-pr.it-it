---
title: Sviluppare app piattaforma UWP (Universal Windows Platform) (UWP)
description: Sviluppare app piattaforma UWP (Universal Windows Platform) (UWP)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3654c1c8773a813fcc7f88b21a86c2ef6049184
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "106299469"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a>Sviluppare app piattaforma UWP (Universal Windows Platform) (UWP)

Invitiamo tutti gli ISV di app desktop (Win32) a portare le app desktop al [piattaforma UWP (Universal Windows Platform) (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) tramite il desktop Bridge. Le app UWP sono supportate anche in [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), quindi risulta più semplice fornire agli utenti un aggiornamento di versione coerente, con conseguente riduzione dei costi di supporto.

Se le app desktop non possono essere convertite tramite desktop Bridge, è consigliabile usare un programma di installazione che segue le procedure consigliate e assicurarsi che sia completamente testato. Un programma di installazione è l'utente o la prima esperienza del cliente con l'app. Troppo spesso, questi programmi non funzionano correttamente o non vengono testati in modo accurato per tutti gli scenari. Il [Kit di certificazione app Windows](https://dev.windows.com/develop/app-certification-kit) consente di testare l'installazione e la disinstallazione dell'app Win32 e di identificare l'uso di API non documentate, oltre ad altri problemi di base relativi alle prestazioni ottimali prima che vengano eseguite dagli utenti.

## <a name="best-practices"></a>Procedure consigliate:

-   Usa programmi di installazione compatibili sia con le versioni a 32 bit che con quelle a 64 bit di Windows.
-   Progetta i programmi di installazione per l'esecuzione in più scenari (livello utente o computer).
-   Mantieni tutti i componenti ridistribuibili Windows nel pacchetto originale. La modifica del pacchetto può causare malfunzionamenti del programma di installazione.
-   Pianifica tempi di sviluppo adeguati per i programmi di installazione. Spesso ne viene sottovalutata l'importanza durante il ciclo di vita di sviluppo del software.

 

 




