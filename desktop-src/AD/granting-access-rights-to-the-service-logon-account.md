---
title: Concessione dei diritti di accesso all'account di accesso al servizio
description: Una considerazione principale dell'installazione di un'istanza del servizio consiste nel garantire che il servizio installato possa accedere alle risorse necessarie.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Concessione dei diritti di accesso all'account di accesso del servizio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f4ea5b85e6158109338b881eeb3f59d74a3910
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299573"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a>Concessione dei diritti di accesso all'account di accesso al servizio

Una considerazione principale dell'installazione di un'istanza del servizio consiste nel garantire che il servizio installato possa accedere alle risorse necessarie. A tale scopo, impostare le voci ACE nei descrittori di sicurezza degli oggetti a cui il servizio deve accedere. Una voce ACE può concedere o negare i diritti di accesso a un'entità di sicurezza specificata, ad esempio l'account utente del servizio o l'account computer per un servizio LocalSystem, oppure un gruppo a cui appartiene l'account del servizio. Per altre informazioni su Ace, descrittori di sicurezza e controllo di accesso, vedere controllo [dell'accesso agli oggetti in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) e [controllo di accesso](/windows/desktop/SecAuthZ/access-control).

Per altre informazioni e un esempio di codice che può essere usato per impostare una voce ACE che consente al servizio di modificare il punto di connessione del servizio, vedere [Abilitazione dell'account del servizio per l'accesso alle proprietà SCP](enabling-service-account-to-access-scp-properties.md).

In alcuni casi, è necessario aggiungere l'account utente del servizio come membro di uno o più gruppi di sicurezza. Se, ad esempio, si crea un gruppo Administrators per il servizio, è possibile rendere il servizio un membro del gruppo. È quindi possibile concedere diritti di accesso al gruppo anziché concederli in modo esplicito all'account del servizio. Per ulteriori informazioni sui gruppi di sicurezza, vedere [gestione dei gruppi](managing-groups.md).

 

 