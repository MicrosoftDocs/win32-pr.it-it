---
title: Concessione dei diritti di accesso all'account di accesso del servizio
description: Una considerazione principale dell'installazione di un'istanza del servizio è garantire che il servizio installato possa accedere alle risorse necessarie.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Concessione dei diritti di accesso all'account di accesso del servizio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d13d3e06432b3501961f65a3e27ca00a46f18197bef23d78e6f7ca0deec59b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189080"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a>Concessione dei diritti di accesso all'account di accesso del servizio

Una considerazione principale dell'installazione di un'istanza del servizio è garantire che il servizio installato possa accedere alle risorse necessarie. A tale scopo, impostare le voci ACE nei descrittori di sicurezza degli oggetti a cui il servizio deve accedere. Una ACE può concedere o negare diritti di accesso a un'entità di sicurezza specificata, ad esempio l'account utente del servizio, l'account computer per un servizio LocalSystem o un gruppo a cui appartiene l'account del servizio. Per altre informazioni su ACE, descrittori di sicurezza e controllo di accesso, vedere Controllo dell'accesso agli oggetti [in](controlling-access-to-objects-in-active-directory-domain-services.md) Active Directory Domain Services e Controllo [di accesso](/windows/desktop/SecAuthZ/access-control).

Per altre informazioni e un esempio di codice che può essere usato per impostare una ACE che consente al servizio di modificare il punto di connessione del servizio, vedere [Abilitazione dell'account](enabling-service-account-to-access-scp-properties.md)del servizio per l'accesso alle proprietà SCP .

In alcuni casi, è necessario aggiungere l'account utente del servizio come membro di uno o più gruppi di sicurezza. Ad esempio, se si crea un gruppo administrators per il servizio, è possibile rendere il servizio un membro del gruppo. È quindi possibile concedere diritti di accesso al gruppo anziché concederli in modo esplicito all'account del servizio. Per altre informazioni sui gruppi di sicurezza, vedere [Gestione dei gruppi](managing-groups.md).

 

 