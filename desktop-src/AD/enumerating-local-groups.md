---
title: Enumerazione di gruppi locali
description: Nei server membri e nei computer in Windows 2000 Professional, è possibile enumerare tutti i gruppi locali.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Enumerazione dei gruppi locali ad Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1584cf8650b3fa341e7a314e0b6f94120b28c50226f16230c53206d6e14b80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191331"
---
# <a name="enumerating-local-groups"></a>Enumerazione di gruppi locali

Nei server membri e nei computer in Windows 2000 Professional, è possibile enumerare tutti i gruppi locali.

È possibile creare solo gruppi locali nei server membri e Windows 2000 Professional. Tuttavia, questi gruppi locali possono contenere:

-   Gruppi universali e globali della foresta che contiene il dominio a cui il computer è membro.
-   Gruppi locali di dominio dal dominio del computer.
-   Utenti di qualsiasi dominio nella foresta.

**Per enumerare i gruppi locali in un server membro o in un computer che esegue Windows 2000 Professional**

1.  Eseguire l'associazione al computer usando le regole seguenti:
    1.  Usare un account con diritti sufficienti per accedere al computer.
    2.  Usare il formato di stringa di associazione seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare ad ADSI che è l'associazione a un computer: "WinNT:// <computer name> , <computer> ".

        "Il <computer name> parametro " è il nome del gruppo di computer a cui accedere. Questo parametro indica ad ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si esegue l'associazione.

    3.  Eseguire l'associazione [**all'interfaccia IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)

2.  Impostare un filtro che contiene "gruppi" usando la [**proprietà IADsContainer.Filter.**](/windows/desktop/api/iads/nn-iads-iadscontainer) In questo modo è possibile enumerare il contenitore e recuperare solo i gruppi.
3.  Enumerare gli oggetti gruppo usando il [**metodo IADsContainer::get \_ \_ NewEnum.**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum)
4.  Per ogni oggetto gruppo, usare [**l'interfaccia IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) per leggere il nome e i membri del gruppo.

 

 