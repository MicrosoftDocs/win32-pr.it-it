---
title: Requisiti di firma delle funzionalità di avvio protetto per i driver in modalità kernel
description: Requisiti di firma delle funzionalità di avvio protetto per i driver in modalità kernel
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05146645e01406fed0129c4f31660509e04581ce889213c7addf01731e45e87f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932171"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a>Requisiti di firma delle funzionalità di avvio protetto per i driver in modalità kernel

## <a name="platforms"></a>Piattaforme

**Client** : Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

In Windows 8 e Windows Server 2012, incluso WinPE, il kernel è stato bloccato per impedire che il malware introdotto dai kit di avvio o radice eviti i requisiti di sicurezza del sistema operativo Windows per i driver firmati.

Questa modifica influisce su tutti i driver in modalità kernel per i dispositivi che supportano l'avvio protetto UEFI (Unified Extensible Firmware Interface). L'avvio protetto UEFI è necessario per Windows 8 per i computer client e facoltativo per i server. Non influisce sui driver in modalità utente.

Lo sviluppo standard per i driver in modalità kernel prevede l'uso del debug in modalità kernel o dell'impostazione dei dati di configurazione di <testsigning> avvio. Entrambi sono disabilitati quando l'avvio protetto è attivata.

## <a name="manifestation"></a>Manifestazione

I driver in modalità kernel non verranno eseguiti se non sono firmati correttamente da un'autorità di certificazione (CA) attendibile. Il sistema operativo non consentirà l'esecuzione di driver non attendibili e non saranno consentiti meccanismi standard come debug del kernel e testsigning.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Per testare i driver, è necessario disabilitare l'avvio protetto nel BIOS e soddisfare gli altri requisiti di firma dei test (vedere di seguito).

Quando si distribuiscono i driver in modo più ampio, è necessario che siano firmati correttamente da un'autorità di certificazione attendibile.

## <a name="resources"></a>Risorse

-   [Firma dei driver](/previous-versions/windows/hardware/design/dn653563(v=vs.85))

 

 