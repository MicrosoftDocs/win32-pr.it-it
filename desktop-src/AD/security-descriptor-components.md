---
title: Componenti del descrittore di sicurezza
description: Dopo aver usato il metodo IADs.Get per recuperare un puntatore a interfaccia IADsSecurityDescriptor, è possibile usare le proprietà IADsSecurityDescriptor per leggere o scrivere i componenti del descrittore di sicurezza di un oggetto directory.
ms.assetid: 35d3d16b-d7fc-4967-ba5c-5a77e058a9ae
ms.tgt_platform: multiple
keywords:
- Componenti del descrittore di sicurezza AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aa5ec61507e56c03bcc3809a2a5eebcb2cbcd36e18f63119aca53448c8a0b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024919"
---
# <a name="security-descriptor-components"></a>Componenti del descrittore di sicurezza

Dopo aver usato il metodo [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) per recuperare un puntatore a interfaccia [**IADsSecurityDescriptor,**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) è possibile usare le proprietà **IADsSecurityDescriptor** per leggere o scrivere i componenti del descrittore di sicurezza di un oggetto directory. Ad esempio, per ottenere o impostare l'elenco DACL dell'oggetto, usare la [**proprietà DiscretionaryAcl.**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods)

Un descrittore di sicurezza può archiviare i dati seguenti:

-   Identificatore di sicurezza (SID) che identifica il proprietario dell'oggetto: il proprietario di un oggetto ha il diritto implicito di modificare l'elenco DACL e i dati del proprietario nel descrittore di sicurezza dell'oggetto.
-   Elenco di controllo di accesso discrezionale (DACL) che identifica gli utenti e i gruppi che possono eseguire diverse operazioni sull'oggetto: un elenco DACL contiene un elenco di voci di controllo di accesso (ACE). Ogni ACE consente o nega un set specificato di diritti di accesso a un account utente, un account di gruppo o un altro fiduciare specificato. Per altre informazioni, vedere [Recupero dell'elenco DACL di un oggetto](retrieving-an-objectampaposs-dacl.md).
-   Elenco sacl (System Access Control List) che controlla il modo in cui il sistema controlla i tentativi di accesso all'oggetto: ogni voce ACE in un SACL specifica i tipi di tentativi di accesso che generano una voce del log di controllo per un account utente, un account di gruppo o un altro fiduciare specificato. Per altre informazioni, vedere [Recupero del SACL di un oggetto](retrieving-an-objectampaposs-sacl.md).
-   Set di flag di controllo **SECURITY \_ DESCRIPTOR \_ CONTROL** che qualificano il significato di un descrittore di sicurezza o dei relativi componenti: ad esempio, il flag **PROTECTED \_ DACL \_** di edizione Standard protegge l'elenco DACL del descrittore di sicurezza dall'ereditarietà delle voci di controllo di accesso dall'oggetto padre.
-   Identificatore di sicurezza (SID) che identifica il gruppo primario dell'oggetto: Active Directory Domain Services questo componente.

Per altre informazioni e un esempio di codice che può essere usato per leggere e visualizzare i dati in un descrittore di sicurezza degli oggetti e in UNCL, vedere Lettura del descrittore di sicurezza [di un oggetto](reading-an-objectampaposs-security-descriptor.md).

 

 