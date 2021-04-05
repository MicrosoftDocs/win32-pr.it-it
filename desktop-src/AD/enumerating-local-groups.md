---
title: Enumerazione dei gruppi locali
description: Nei server membri e nei computer in cui è in esecuzione Windows 2000 Professional è possibile enumerare tutti i gruppi locali.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Enumerazione dei gruppi locali AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e106fc2517cfedd8fb5fa40e4b99798ee32de8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724554"
---
# <a name="enumerating-local-groups"></a>Enumerazione dei gruppi locali

Nei server membri e nei computer in cui è in esecuzione Windows 2000 Professional è possibile enumerare tutti i gruppi locali.

Nei server membri e in Windows 2000 Professional è possibile creare solo gruppi locali. Tuttavia, tali gruppi locali possono contenere:

-   Gruppi universali e globali dalla foresta che contiene il dominio al quale appartiene il computer.
-   Gruppi locali di dominio dal dominio del computer.
-   Utenti di qualsiasi dominio nella foresta.

**Per enumerare i gruppi locali in un server membro o in un computer che esegue Windows 2000 Professional**

1.  Eseguire l'associazione al computer utilizzando le regole seguenti:
    1.  Utilizzare un account con diritti sufficienti per accedere a tale computer.
    2.  Usare il formato stringa di binding seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare a ADSI che è in associazione a un computer: "WinNT:// <computer name> <computer> ".

        Il parametro "The <computer name> " è il nome del gruppo di computer a cui accedere. Questo parametro indica a ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione ambiguità per determinare il tipo di oggetto a cui si sta effettuando l'associazione.

    3.  Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .

2.  Impostare un filtro che contenga "gruppi" utilizzando la proprietà [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) . In questo modo è possibile enumerare il contenitore e recuperare solo i gruppi.
3.  Enumerare gli oggetti Group usando il metodo [**IADsContainer:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) .
4.  Per ogni oggetto gruppo, utilizzare l'interfaccia [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) per leggere il nome e i membri del gruppo.

 

 