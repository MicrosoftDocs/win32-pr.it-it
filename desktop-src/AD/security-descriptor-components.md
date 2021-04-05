---
title: Componenti del descrittore di sicurezza
description: Avendo usato il metodo IADs. Get per recuperare un puntatore all'interfaccia IADsSecurityDescriptor, è possibile usare le proprietà IADsSecurityDescriptor per leggere o scrivere i componenti del descrittore di sicurezza di un oggetto directory.
ms.assetid: 35d3d16b-d7fc-4967-ba5c-5a77e058a9ae
ms.tgt_platform: multiple
keywords:
- AD di componenti del descrittore di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef87b0e23f60fdbb4d0b03b421012d5918ed3c83
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724423"
---
# <a name="security-descriptor-components"></a>Componenti del descrittore di sicurezza

Avendo usato il metodo [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) per recuperare un puntatore all'interfaccia [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) , è possibile usare le proprietà **IADsSecurityDescriptor** per leggere o scrivere i componenti del descrittore di sicurezza di un oggetto directory. Per ottenere o impostare l'elenco DACL dell'oggetto, ad esempio, usare la proprietà [**DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) .

Un descrittore di sicurezza può archiviare i dati seguenti:

-   Un ID di sicurezza (SID) che identifica il proprietario dell'oggetto: il proprietario di un oggetto dispone del diritto implicito per modificare i dati DACL e Owner nel descrittore di sicurezza dell'oggetto.
-   Elenco di controllo di accesso discrezionale (DACL) che identifica gli utenti e i gruppi che possono eseguire varie operazioni sull'oggetto: un DACL contiene un elenco di voci di controllo di accesso (ACE). Ogni voce ACE consente o nega un set specificato di diritti di accesso a un account utente, un account di gruppo o un altro trustee specificato. Per ulteriori informazioni, vedere [recupero del DACL di un oggetto](retrieving-an-objectampaposs-dacl.md).
-   Elenco di controllo di accesso di sistema (SACL) che controlla il modo in cui il sistema controlla i tentativi di accesso all'oggetto. ogni voce ACE in un SACL specifica i tipi di tentativi di accesso che generano una voce del registro di controllo per un account utente specificato, un account di gruppo o un altro trustee. Per ulteriori informazioni, vedere [recupero del SACL di un oggetto](retrieving-an-objectampaposs-sacl.md).
-   Set di flag di controllo del controllo del **\_ descrittore \_ di sicurezza** che qualificano il significato di un descrittore di sicurezza o dei relativi componenti. ad esempio, il flag di controllo **\_ DACL se \_** protegge il DACL del descrittore di sicurezza dalle voci ACE ereditate dall'oggetto padre.
-   Un ID di sicurezza (SID) che identifica il gruppo primario dell'oggetto: Active Directory Domain Services non usare questo componente.

Per ulteriori informazioni e un esempio di codice che può essere utilizzato per leggere e visualizzare i dati in un descrittore di sicurezza dell'oggetto e un DACL, vedere [lettura del descrittore di sicurezza di un oggetto](reading-an-objectampaposs-security-descriptor.md).

 

 