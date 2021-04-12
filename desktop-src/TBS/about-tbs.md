---
title: Informazioni su TBS
description: Servizio di sistema che consente la condivisione trasparente delle risorse del Trusted Platform Module (TPM).
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- Servizi di base TPM TBS, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5d40b1fca688676978f274cb976afedb6e6a56
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104223400"
---
# <a name="about-tbs"></a>Informazioni su TBS

La funzionalità Servizi di base TPM (TBS) è un servizio di sistema che consente la condivisione trasparente delle risorse del Trusted Platform Module (TPM). Condivide contemporaneamente le risorse TPM tra più applicazioni nello stesso computer fisico, anche se tali applicazioni vengono eseguite in macchine virtuali diverse. A partire da Windows 8 e Windows Server 2012, TBS è preinstallato in tutti i sistemi con un TPM.

Il Trusted Computing Group (TCG) definisce una Trusted Platform Module che fornisce funzioni di crittografia progettate per fornire attendibilità alla piattaforma. Poiché il TPM è implementato nell'hardware, dispone di risorse finite. Il TCG definisce anche uno stack software che usa queste risorse per fornire operazioni attendibili per il software applicativo. Tuttavia, non viene effettuato alcun provisioning per l'esecuzione side-by-side di un'implementazione di TSS con software del sistema operativo che può utilizzare anche risorse TPM. La funzionalità TBS risolve questo problema abilitando ogni stack software che comunica con TBS per usare le risorse TPM per verificare la presenza di altri stack software che potrebbero essere in esecuzione nel computer.

Le specifiche TPM e lo stack software TCG (TSS) sono disponibili all'indirizzo [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .

TBS viene implementato come servizio out-of-process che accetta i comandi che usano un servizio RPC. Una libreria collegata dinamicamente presenta l'interfaccia del linguaggio C e comunica con il servizio TBS.

> [!Note]  
> Il servizio TBS accetta solo le richieste RPC dal computer locale.

 

Gli obiettivi principali di TBS sono:

-   Fornire una condivisione efficiente di risorse TPM limitate, ad esempio slot chiave, slot di sessioni di autorizzazione e slot di trasporto.
-   Fornire l'accesso in ordine di priorità e sincronizzato alle risorse TPM tra più istanze di stack di software TPM.
-   Fornire una gestione appropriata delle risorse TPM tra gli Stati di alimentazione.
-   Impedire agli stack di software TPM di accedere ai comandi TPM che devono essere limitati a causa di limitazioni della piattaforma o requisiti amministrativi.

Nella figura seguente viene illustrata la relazione tra TBS e il TPM.

![relazione di TBS in modalità utente con il TPM in modalità kernel](images/tbs-block-diagram-as11601.png)

 

 




