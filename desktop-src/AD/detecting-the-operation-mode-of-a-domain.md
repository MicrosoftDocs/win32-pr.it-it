---
title: Rilevamento della modalità operativa di un dominio
description: In Windows 2000, un dominio può essere eseguito in due modalità operative miste e native.
ms.assetid: c20dec14-50ad-4f63-bd5c-222c2f2c83e4
ms.tgt_platform: multiple
keywords:
- Rilevamento della modalità operativa di un dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d871bd50c9a7462972992685d4226963a3eaff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872325"
---
# <a name="detecting-the-operation-mode-of-a-domain"></a>Rilevamento della modalità operativa di un dominio

In Windows 2000, un dominio può essere eseguito in due modalità operative: misto e nativo. Utilizzare la modalità mista per includere i controller di dominio che eseguono Windows NT 4,0 in un dominio Windows 2000. La modalità mista non supporta i gruppi universali o i gruppi annidati. Se tutti i controller di dominio nel dominio eseguono Windows 2000, è possibile utilizzare la modalità nativa.

Per rilevare a livello di codice la modalità operativa di un dominio di Windows 2000, leggere la proprietà [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) dell'oggetto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) per quel dominio. Il valore zero (0) indica che il dominio è in modalità nativa. Un valore pari a uno (1) indica che il dominio è in modalità mista. È anche possibile usare la funzione [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) per ottenere la modalità operativa, nonché altri dati sul dominio e il relativo stato.

Per eseguire il binding all'oggetto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) del dominio dell'account utente con cui è in esecuzione l'applicazione, usare binding senza server e RootDSE per ottenere il nome distinto per il dominio e quindi usare tale nome distinto per l'associazione all'oggetto **domainDNS** che rappresenta tale dominio. Per ulteriori informazioni sull'associazione senza server e rootDSE, vedere [binding senza server e RootDSE](serverless-binding-and-rootdse.md).

Per ulteriori informazioni e un esempio di codice in cui viene illustrato come rilevare a livello di codice la modalità operativa di un dominio, vedere [il codice di esempio per determinare la modalità operativa](example-code-for-determining-the-operation-mode.md).

 

 