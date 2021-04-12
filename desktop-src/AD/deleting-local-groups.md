---
title: Eliminazione di gruppi locali
description: In questo argomento viene illustrato come eliminare un gruppo locale da un server membro o da un computer che esegue Windows 2000 Professional.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Eliminazione di gruppi locali AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b55f90a8e6ac5cb77bf878d5ac680a6da91f73
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472603"
---
# <a name="deleting-local-groups"></a>Eliminazione di gruppi locali

In questo argomento viene illustrato come eliminare un gruppo locale da un server membro o da un computer che esegue Windows 2000 Professional.

**Per eliminare un gruppo locale**

1.  Eseguire l'associazione al computer utilizzando le regole seguenti:
    1.  Utilizzare un account con diritti sufficienti per accedere a tale computer.
    2.  Usare il formato stringa di binding seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare a ADSI che è in associazione a un computer: "WinNT:// <computer name> <computer> ". Il &lt; parametro "nome computer &gt; " è il nome del gruppo di computer a cui accedere. Questo parametro indica a ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione ambiguità per determinare il tipo di oggetto a cui si sta effettuando l'associazione.
    3.  Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Specificare "Group" come classe usando [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)per eliminare il gruppo.

    Non è necessario chiamare [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) per eseguire il commit della modifica nel contenitore. La chiamata a [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) consente di eseguire il commit dell'eliminazione del gruppo direttamente nella directory.

 

 