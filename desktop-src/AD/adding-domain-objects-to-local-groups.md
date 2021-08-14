---
title: Aggiunta di oggetti di dominio a gruppi locali
description: Gli utenti e i gruppi che appartengono al dominio possono essere aggiunti ai gruppi nel computer locale per concedere diritti all'utente o al gruppo di dominio nel computer specifico.
ms.assetid: 07287190-88a1-4d4d-a91c-1e95d9903a4d
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory , aggiunta di oggetti di dominio a gruppi locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea9e3334510da0827692141d511be173b56683bafe6b80f8a0247ae241125a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024924"
---
# <a name="adding-domain-objects-to-local-groups"></a>Aggiunta di oggetti di dominio a gruppi locali

Quando un server membro o un computer in esecuzione in Windows 2000 Professional è membro di un dominio di Windows 2000, gli utenti e i gruppi che appartengono al dominio possono essere aggiunti ai gruppi nel computer locale per concedere diritti all'utente o al gruppo di dominio nel computer specifico.

Quando si gestiscono gruppi locali di dominio in Windows 2000 usando ADSI, viene in genere usato il provider LDAP. Quando si gestiscono gruppi locali nei server membri e in un computer Windows 2000 Professional, tuttavia, è necessario usare il provider WinNT.

È possibile creare solo gruppi locali nei server membri e Windows 2000 Professional. Tuttavia, i gruppi locali possono contenere:

-   Gruppi universali e globali della foresta che contiene il dominio di cui il computer è membro.
-   Gruppi locali di dominio da tale dominio del computer.
-   Utenti di qualsiasi dominio nella foresta.

**Per aggiungere un oggetto di dominio a un gruppo locale**

1.  Eseguire il binding [**all'interfaccia IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) del computer che contiene il gruppo locale a cui aggiungere un membro. L'associazione deve essere eseguita usando un account con diritti sufficienti per accedere al computer. La stringa di associazione deve avere il formato "WinNT:// ,computer", dove " nome computer " è il nome del gruppo di computer a cui <computer name> &lt; aggiungere un &gt; membro. Il parametro ",computer" indica ad ADSI che è un'associazione a un computer. ADSI espone questi dati al parser del provider WinNT in modo che possa ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si esegue l'associazione. In questo modo l'utente può attendere da 5 a 20 secondi che l'ambiguità sia risolta.
2.  Usare il [**metodo IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) con "group" come classe e il nome del gruppo locale come nome dell'oggetto da associare al gruppo.
3.  Eseguire il binding [**all'interfaccia IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) del gruppo locale a cui verrà aggiunto un membro.
4.  Costruire l'ADsPath dell'oggetto da aggiungere al gruppo locale nel formato "WinNT://", dove " dominio " è il nome del dominio che contiene l'oggetto da aggiungere e " nome " è il nome dell'oggetto <domain> / <name> &lt; da &gt; &lt; &gt; aggiungere.
5.  Aggiungere l'utente o il gruppo al gruppo locale con il [**metodo IADsGroup.Add,**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) passando il percorso ADsPath costruito nel passaggio 4.

Per altre informazioni e un esempio di codice che illustra come aggiungere un oggetto utente o gruppo di dominio a un gruppo locale, vedere Codice di esempio per l'aggiunta di un utente o di un gruppo di dominio [a un gruppo locale.](example-code-for-adding-a-domain-user-or-group-to-a-local-group.md)

 

 