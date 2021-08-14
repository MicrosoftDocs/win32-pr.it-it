---
title: Informazioni sui TB
description: Servizio di sistema che consente la condivisione trasparente delle Trusted Platform Module (TPM).
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- TPM Base Services TBS , about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4997bf6181a1da7aabaf811d0f1d0cf3e3ca813bb11a8f2d73b3b286e4e5ebde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954454"
---
# <a name="about-tbs"></a>Informazioni sui TB

La funzionalità Servizi di base TPM (TBS) è un servizio di sistema che consente la condivisione trasparente delle risorse Trusted Platform Module (TPM). Condivide contemporaneamente le risorse TPM tra più applicazioni nello stesso computer fisico, anche se tali applicazioni vengono eseguite in macchine virtuali diverse. A partire Windows 8 e Windows Server 2012, TBS è preinstallato in tutti i sistemi con un TPM.

Il Trusted Computing Group (TCG) definisce un Trusted Platform Module che fornisce funzioni di crittografia progettate per fornire attendibilità nella piattaforma. Poiché il TPM è implementato nell'hardware, dispone di risorse limitate. Il TCG definisce anche uno stack software che usa queste risorse per fornire operazioni attendibili per il software applicativo. Tuttavia, non viene effettuato alcun provisioning per l'esecuzione side-by-side di un'implementazione TSS con software del sistema operativo che potrebbe anche usare risorse TPM. La funzionalità TBS risolve questo problema consentendo a ogni stack software che comunica con TBS di usare le risorse TPM per verificare la presenza di altri stack software che potrebbero essere in esecuzione nel computer.

La specifica TPM e la specifica TCG Software Stack (TSS) sono disponibili all'indirizzo [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .

TbS viene implementato come servizio out-of-process che accetta comandi che usano un servizio RPC. Una libreria collegata dinamicamente presenta l'interfaccia del linguaggio C e comunica con il servizio TBS.

> [!Note]  
> Il servizio TBS accetta solo le richieste RPC dal computer locale.

 

Gli obiettivi principali dei tbs sono:

-   Offrire una condivisione efficiente di risorse TPM limitate, ad esempio slot chiave, slot di sessioni di autorizzazione e slot di trasporto.
-   Fornire l'accesso con priorità e sincronizzato alle risorse TPM tra più istanze di stack di software TPM.
-   Fornire una gestione appropriata delle risorse TPM tra stati di alimentazione.
-   Impedire agli stack di software TPM di accedere ai comandi TPM che devono essere limitati, a causa di limitazioni della piattaforma o requisiti amministrativi.

La figura seguente mostra la relazione tra i tbs e il TPM.

![relazione tra i tb in modalità utente e il tpm in modalità kernel](images/tbs-block-diagram-as11601.png)

 

 




