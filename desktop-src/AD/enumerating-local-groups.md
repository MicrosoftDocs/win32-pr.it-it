---
title: Enumerazione di gruppi locali
description: Nei server membri e nei computer in Windows 2000 Professional, è possibile enumerare tutti i gruppi locali.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Enumerazione dei gruppi locali AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcecf0f16cb0679e190197f0677cb9b23a96195
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881426"
---
# <a name="enumerating-local-groups"></a>Enumerazione di gruppi locali

Nei server membri e nei computer in Windows 2000 Professional, è possibile enumerare tutti i gruppi locali.

Solo i gruppi locali possono essere creati nei server membri e Windows 2000 Professional. Tuttavia, questi gruppi locali possono contenere:

-   Gruppi universali e globali della foresta che contiene il dominio di cui il computer è membro.
-   Gruppi locali di dominio dal dominio del computer.
-   Utenti di qualsiasi dominio nella foresta.

**Per enumerare i gruppi locali in un server membro o in un computer che esegue Windows 2000 Professional**

1.  Eseguire il binding al computer usando le regole seguenti:
    1.  Usare un account con diritti sufficienti per accedere al computer.
    2.  Usare il formato di stringa di associazione seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare ad ADSI che è in associazione a un computer: "WinNT:// <computer name> , &lt; computer &gt; ".

        "Il <computer name> parametro " è il nome del gruppo di computer a cui accedere. Questo parametro indica ad ADSI che è in fase di associazione a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si esegue l'associazione.

    3.  Eseguire il binding [**all'interfaccia IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)

2.  Impostare un filtro che contiene "gruppi" usando la [**proprietà IADsContainer.Filter.**](/windows/desktop/api/iads/nn-iads-iadscontainer) In questo modo è possibile enumerare il contenitore e recuperare solo i gruppi.
3.  Enumerare gli oggetti gruppo usando il [**metodo IADsContainer::get \_ \_ NewEnum.**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum)
4.  Per ogni oggetto gruppo, usare [**l'interfaccia IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) per leggere il nome e i membri del gruppo.

 

 
