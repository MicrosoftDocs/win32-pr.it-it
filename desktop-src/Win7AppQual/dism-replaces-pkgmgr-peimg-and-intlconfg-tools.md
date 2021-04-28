---
description: Gestione e manutenzione immagini distribuzione
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Gestione e manutenzione immagini distribuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d16233927dca2d5dba296fd33fb64135f691e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088489"
---
# <a name="deployment-image-servicing-and-management-dism"></a>Gestione e manutenzione immagini distribuzione

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows Vista SP1 e versioni successive \| windows 7  
**Server** - Windows Server 2008 RTM e versioni successive \| Windows Server 2008 R2  


## <a name="description"></a>Descrizione

Lo Gestione e manutenzione immagini distribuzione (DISM) sostituisce gli strumenti pkgmgr, PEImg e IntlConfg ritirati in Windows 7. Gestione e manutenzione immagini distribuzione offre un unico strumento centralizzato per eseguire tutte le funzioni di questi tre strumenti in modo più efficiente e standardizzato, eliminando la fonte di molte delle frustrazioni riscontrate dagli attuali utenti di questi strumenti.

Gestione e manutenzione immagini distribuzione include uno shim per Windows Vista SP1 e versioni successive, nonché per Windows Server 2008 RTM e versioni successive, che reindirizza le chiamate pkgmgr da applicazioni legacy in esecuzione in Windows 7 a Gestione e manutenzione immagini distribuzione. Se l'applicazione è in esecuzione in uno dei sistemi operativi supportati, lo shim instrada la chiamata a pkgmgr. Non esistono s shims per le applicazioni legacy che chiamano PEImg o IntlConfg.

## <a name="usage"></a>Utilizzo

Gestione e manutenzione immagini distribuzione è trasparente per gli utenti finali di pkgmgr in una delle piattaforme supportate. Tuttavia, se un'applicazione chiama PEImg o IntlConfg da Windows 7, la chiamata avrà esito negativo.

Aggiornare gli script che chiamano pkgmgr, PEImg o IntlConfg per chiamare invece Gestione e manutenzione immagini distribuzione. È importante includere l'aggiornamento degli script pkgmgr in questo sforzo, poiché lo shim che fornisce la compatibilità con le versioni precedenti per pkgmgr verrà rimosso nelle versioni future dei sistemi operativi Windows.

Verificare che le chiamate a Gestione e manutenzione immagini distribuzione siano state sostituite da qualsiasi chiamata a pkgmgr, PEImg e IntlConfg e che l'operazione sia stata eseguita correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione e manutenzione immagini distribuzione (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))
</dt> </dl>

 

 
