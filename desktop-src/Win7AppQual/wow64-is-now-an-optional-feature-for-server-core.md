---
description: WoW64 è ora una funzionalità facoltativa per Server Core
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: Stato di WoW64 in Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f836d361e172527bf23c7e51ea0071790d3857d6611d8a12ff62185226d3f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994471"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a>WoW64 è ora una funzionalità facoltativa per Server Core

## <a name="affected-platforms"></a>Piattaforme interessate

**Server** - Windows Server 2008 R2  



## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Bassa  





## <a name="description"></a>Descrizione

L'opzione di installazione Server Core per Windows Server 2008 R2 consente di disinstallare WoW64. WoW64 è ora una funzionalità facoltativa che è possibile disinstallare se non è necessario eseguire codice a 32 bit.

Inoltre, i ruoli Active Directory e Active Directory Lightweight Directory Services richiedono WoW64 per l'esecuzione in Windows Server 2008 R2.

## <a name="manifestation-of-impact"></a>Manifestazione di impatto

Se si disinstalla WoW64, gli amministratori che eseguono codice a 32 bit in Server Core riceveranno un messaggio di errore che indica che l'applicazione non può essere eseguita. Se gli amministratori tentano di eseguire Active Directory Active Directory Lightweight Directory Services, riceveranno un messaggio di errore.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Installare WoW64.

## <a name="solution"></a>Soluzione

La soluzione preferita consiste nel fornire una versione a 64 bit del codice per consentire l'esecuzione in Server Core senza la necessità di WoW64.

Fornire almeno la documentazione dell'utente che indica che per eseguire codice a 32 bit è necessario installare WoW64.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

Verificare che tutto il codice usato sia a 64 bit.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Dettagli sull'implementazione di WOW64](../winprog64/wow64-implementation-details.md)
-   [Debug di WOW64](../winprog64/debugging-wow64.md)
-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 
