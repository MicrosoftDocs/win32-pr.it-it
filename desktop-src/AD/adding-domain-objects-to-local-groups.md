---
title: Aggiunta di oggetti di dominio ai gruppi locali
description: Gli utenti e i gruppi che appartengono al dominio possono essere aggiunti ai gruppi nel computer locale per concedere diritti all'utente o al gruppo del dominio in quel particolare computer.
ms.assetid: 07287190-88a1-4d4d-a91c-1e95d9903a4d
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, aggiunta di oggetti di dominio ai gruppi locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e956d1cf076f4c33c46700e52798463b7e1d2c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724663"
---
# <a name="adding-domain-objects-to-local-groups"></a>Aggiunta di oggetti di dominio ai gruppi locali

Quando un server membro o un computer in cui è in esecuzione Windows 2000 Professional è membro di un dominio di Windows 2000, gli utenti e i gruppi che appartengono al dominio possono essere aggiunti ai gruppi nel computer locale per concedere diritti all'utente o al gruppo del dominio in quel particolare computer.

Quando si gestiscono gruppi locali di dominio in un dominio Windows 2000 usando ADSI, viene in genere usato il provider LDAP. Quando si gestiscono gruppi locali su server membri e un computer che esegue Windows 2000 Professional, è necessario utilizzare il provider WinNT.

Nei server membri e in Windows 2000 Professional è possibile creare solo gruppi locali. Tuttavia, i gruppi locali possono contenere:

-   Gruppi universali e globali dalla foresta che contiene il dominio di cui è membro il computer.
-   Gruppi locali di dominio da tale dominio del computer.
-   Utenti di qualsiasi dominio nella foresta.

**Per aggiungere un oggetto di dominio a un gruppo locale**

1.  Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) del computer che contiene il gruppo locale a cui aggiungere un membro. L'associazione deve essere eseguita utilizzando un account con diritti sufficienti per accedere a tale computer. La stringa di associazione deve avere il formato "WinNT:// <computer name> , computer" dove " &lt; nome computer &gt; " è il nome del gruppo di computer a cui aggiungere un membro. Il parametro ", computer" indica a ADSI che è in associazione a un computer. ADSI espone questi dati al parser del provider WinNT, in modo che possa ignorare alcune query di risoluzione ambiguità per determinare il tipo di oggetto a cui si sta effettuando l'associazione. Questo consente di salvare l'utente da 5 a 20 secondi di attesa per la risoluzione dell'ambiguità.
2.  Usare il metodo [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) con "Group" come classe e il nome del gruppo locale come nome dell'oggetto da associare al gruppo.
3.  Eseguire l'associazione all'interfaccia [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) del gruppo locale a cui verrà aggiunto un membro.
4.  Costruire il ADsPath dell'oggetto da aggiungere al gruppo locale nel formato "WinNT:// <domain> / <name> ", dove " &lt; dominio &gt; " è il nome del dominio che contiene l'oggetto da aggiungere e " &lt; nome &gt; " è il nome dell'oggetto da aggiungere.
5.  Aggiungere l'utente o il gruppo al gruppo locale con il metodo [**IADsGroup. Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) , passando il ADsPath costruito nel passaggio 4.

Per ulteriori informazioni e un esempio di codice in cui viene illustrato come aggiungere un utente di dominio o un oggetto gruppo a un gruppo locale, vedere il [codice di esempio per l'aggiunta di un utente o gruppo di dominio a un gruppo locale](example-code-for-adding-a-domain-user-or-group-to-a-local-group.md).

 

 