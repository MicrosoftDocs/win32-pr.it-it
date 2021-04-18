---
description: .
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Gestione e manutenzione immagini distribuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734ac9fae497eeb61d706a228fc1ffc6ea4da264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318579"
---
# <a name="deployment-image-servicing-and-management-dism"></a>Gestione e manutenzione immagini distribuzione

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** -Windows Vista SP1 e versioni successive \| Windows 7  
**Server** : windows Server 2008 RTM e versioni successive \| Windows Server 2008 R2  


## <a name="description"></a>Descrizione

Lo strumento Gestione e manutenzione immagini distribuzione (DISM) sostituisce gli strumenti pkgmgr, PEImg e IntlConfg che vengono ritirati in Windows 7. DISM fornisce un unico strumento centralizzato per l'esecuzione di tutte le funzioni di questi tre strumenti in modo più efficiente e standardizzato, eliminando l'origine di molte delle frustrazioni riscontrate dagli utenti correnti di questi strumenti.

DISM include uno shim per Windows Vista SP1 e versioni successive, nonché per Windows Server 2008 RTM e versioni successive, che reindirizza le chiamate pkgmgr da applicazioni legacy in esecuzione su Windows 7 a DISM. Se l'applicazione è in esecuzione in uno dei sistemi operativi supportati, lo shim instrada la chiamata a pkgmgr. Non esistono shim per le applicazioni legacy che chiamano PEImg o IntlConfg.

## <a name="usage"></a>Utilizzo

DISM è trasparente per gli utenti finali di pkgmgr su qualsiasi piattaforma supportata. Tuttavia, se un'applicazione chiama PEImg o IntlConfg da Windows 7, la chiamata avrà esito negativo.

Aggiornare tutti gli script che chiamano pkgmgr, PEImg o IntlConfg per chiamare gestione e manutenzione immagini distribuzione. È importante includere l'aggiornamento degli script pkgmgr in questo sforzo, perché lo shim che fornisce la compatibilità con le versioni precedenti di pkgmgr verrà rimosso nelle versioni future dei sistemi operativi Windows.

Verificare che le chiamate a DISM abbiano sostituito le chiamate a pkgmgr, PEImg e IntlConfg e che l'operazione venga eseguita correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione e manutenzione immagini distribuzione (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))
</dt> </dl>

 

 
