---
description: Gestione e manutenzione immagini distribuzione
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Gestione e manutenzione immagini distribuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6da1cc8ec3e77a6c63df8e44917cb5f3474ae8e7a5e34b58f49255fa34b5b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053179"
---
# <a name="deployment-image-servicing-and-management-dism"></a>Gestione e manutenzione immagini distribuzione

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows Vista SP1 e versioni successive \| Windows 7  
**Server** - Windows Server 2008 RTM e versioni successive \| Windows Server 2008 R2  


## <a name="description"></a>Descrizione

Lo Gestione e manutenzione immagini distribuzione (DISM) sostituisce gli strumenti pkgmgr, PEImg e IntlConfg ritirati in Windows 7. Gestione e manutenzione immagini distribuzione offre un unico strumento centralizzato per eseguire tutte le funzioni di questi tre strumenti in modo più efficiente e standardizzato, eliminando l'origine di molte delle frustrazioni riscontrate dagli utenti correnti di questi strumenti.

Gestione e manutenzione immagini distribuzione include uno shim per Windows Vista SP1 e versioni successive, nonché per Windows Server 2008 RTM e versioni successive, che reindirizza le chiamate pkgmgr dalle applicazioni legacy in esecuzione in Windows 7 a Gestione e manutenzione immagini distribuzione. Se l'applicazione è in esecuzione in uno dei sistemi operativi supportati, lo shim instrada la chiamata a pkgmgr. Non esistono s shim per le applicazioni legacy che chiamano PEImg o IntlConfg.

## <a name="usage"></a>Utilizzo

Gestione e manutenzione immagini distribuzione è trasparente per gli utenti finali di pkgmgr in una delle piattaforme supportate. Tuttavia, se un'applicazione chiama PEImg o IntlConfg da Windows 7, la chiamata avrà esito negativo.

Aggiornare gli script che chiamano pkgmgr, PEImg o IntlConfg per chiamare invece Gestione e manutenzione immagini distribuzione. È importante includere l'aggiornamento degli script pkgmgr in questo lavoro, perché lo shim che garantisce la compatibilità con le versioni precedenti di pkgmgr verrà rimosso nelle versioni future dei sistemi operativi Windows.

Verificare che le chiamate a Gestione e manutenzione immagini distribuzione siano state sostituite da pkgmgr, PEImg e IntlConfg e che l'operazione sia stata eseguita correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione e manutenzione immagini distribuzione (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))
</dt> </dl>

 

 
