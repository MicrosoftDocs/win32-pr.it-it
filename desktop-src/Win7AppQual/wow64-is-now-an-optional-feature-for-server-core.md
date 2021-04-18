---
description: .
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Stato WoW64 in Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a121c6bb9c4fb2cd052825bb4c2d5e3dbd0183c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318563"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a>WoW64 è ora una funzionalità facoltativa per Server Core

## <a name="affected-platforms"></a>Piattaforme interessate

**Server** -Windows Server 2008 R2  



## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -bassa  
**Frequenza** -bassa  





## <a name="description"></a>Descrizione

L'opzione di installazione dei componenti di base del server per Windows Server 2008 R2 consente di disinstallare WoW64. WoW64 è ora una funzionalità facoltativa che è possibile disinstallare se non è necessario eseguire codice a 32 bit.

Inoltre, per l'esecuzione in Windows Server 2008 R2, i ruoli Active Directory e Active Directory Lightweight Directory Services richiedono WoW64.

## <a name="manifestation-of-impact"></a>Manifesto di effetto

Se si disinstalla WoW64, gli amministratori che eseguono codice a 32 bit in Server Core riceveranno un messaggio di errore che segnala che non è possibile eseguire l'applicazione. Se gli amministratori tentano di eseguire Active Directory e Active Directory Lightweight Directory Services, riceveranno un messaggio di errore.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Installare WoW64.

## <a name="solution"></a>Soluzione

La soluzione preferita consiste nel fornire una versione a 64 bit del codice per consentirne l'esecuzione in Server Core senza la necessità di WoW64.

Fornire almeno la documentazione utente nota per eseguire codice a 32 bit, è necessario installare WoW64.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilità, prestazioni, affidabilità e test di usabilità

Verificare che tutto il codice utilizzato sia a 64 bit.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Dettagli di implementazione di WOW64](../winprog64/wow64-implementation-details.md)
-   [Debug di WOW64](../winprog64/debugging-wow64.md)
-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 
