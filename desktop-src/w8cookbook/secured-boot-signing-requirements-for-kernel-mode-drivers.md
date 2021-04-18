---
title: Requisiti di firma delle funzionalità di avvio protetto per i driver in modalità kernel
description: Requisiti di firma delle funzionalità di avvio protetto per i driver in modalità kernel
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a63a8b1fca1677aa125bac96dfec290dcd736b5
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300567"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a>Requisiti di firma delle funzionalità di avvio protetto per i driver in modalità kernel

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

In Windows 8 e Windows Server 2012, incluso WinPE, il kernel è stato bloccato per impedire che malware introdotto da boot o kit radice eludesse i requisiti di sicurezza del sistema operativo Windows per i driver firmati.

Questa modifica ha effetto su tutti i driver in modalità kernel per i dispositivi che supportano l'avvio protetto UEFI (Unified Extensible Firmware Interface). L'avvio protetto UEFI è necessario per la certificazione di Windows 8 per i computer client e facoltativa per i server. Non influisce sui driver in modalità utente.

Lo sviluppo standard per i driver in modalità kernel comporta l'utilizzo del debug in modalità kernel o dell'impostazione dati di configurazione di avvio (BCD) <testsigning> . Entrambi sono disabilitati quando è abilitato l'avvio protetto.

## <a name="manifestation"></a>Manifestazione

I driver in modalità kernel non verranno eseguiti se non sono firmati correttamente da un'autorità di certificazione (CA) attendibile. Il sistema operativo non consentirà l'esecuzione di driver non attendibili e i meccanismi standard come il debug del kernel e testsigning non saranno consentiti.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Per testare i driver, è necessario disabilitare l'avvio protetto nel BIOS e soddisfare gli altri requisiti di firma dei test (vedere di seguito).

Quando si distribuiscono i driver più ampiamente, devono essere firmati correttamente da un'autorità di certificazione attendibile.

## <a name="resources"></a>Risorse

-   [Firma dei driver](/previous-versions/windows/hardware/design/dn653563(v=vs.85))

 

 