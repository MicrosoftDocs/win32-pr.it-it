---
title: Requisiti di firma delle funzionalità di avvio sicuro per i driver in modalità kernel
description: Requisiti di firma delle funzionalità di avvio sicuro per i driver in modalità kernel
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6593df6707dc26b36fceca796c436ed45f3f0c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885069"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a>Requisiti di firma delle funzionalità di avvio sicuro per i driver in modalità kernel

## <a name="platforms"></a>Piattaforme

**Client** : Windows 8  
**Server** - Windows Server 2012  


## <a name="description"></a>Descrizione

In Windows 8 e Windows Server 2012, incluso WinPE, il kernel è stato bloccato per impedire al malware introdotto dai kit di avvio o radice di aggirare Windows requisiti di sicurezza del sistema operativo per i driver firmati.

Questa modifica influisce su tutti i driver in modalità kernel per i dispositivi che supportano l'avvio sicuro UEFI (Unified Extensible Firmware Interface). L'avvio sicuro UEFI è necessario per Windows 8 per i computer client e facoltativo per i server. Non influisce sui driver in modalità utente.

Lo sviluppo standard per i driver in modalità kernel prevede l'uso del debug in modalità kernel o dell'impostazione di test dei dati di configurazione di &lt; avvio (BCD). &gt; Entrambi sono disabilitati quando l'avvio protetto è attivata.

## <a name="manifestation"></a>Manifestazione

I driver in modalità kernel non verranno eseguiti se non sono firmati correttamente da un'autorità di certificazione (CA) attendibile. Il sistema operativo non consentirà l'esecuzione di driver non attendibili e non saranno consentiti meccanismi standard come debug del kernel e testsigning.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Per testare i driver, è necessario disabilitare l'avvio sicuro nel BIOS e soddisfare gli altri requisiti di firma dei test (vedere di seguito).

Quando si distribuiscono i driver in modo più ampio, devono essere firmati correttamente da una CA attendibile.

## <a name="resources"></a>Risorse

-   [Firma dei driver](/previous-versions/windows/hardware/design/dn653563(v=vs.85))

 

 
