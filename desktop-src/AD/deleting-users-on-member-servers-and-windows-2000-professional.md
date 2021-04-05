---
title: Eliminazione di utenti su server membri e Windows 2000 Professional
description: In questo argomento viene illustrato come eliminare un utente da un server membro o da un computer che esegue Windows 2000 Professional.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- utenti AD, eliminazione di un utente nei server membri e Windows 2000 Professional
- Active Directory, utilizzo di, utenti, eliminazione di utenti su server membri e Windows 2000 Professional
- eliminazione di un utente
- Server, eliminazione di un utente
- eliminazione di utenti su server membri e Windows 2000 Professional AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae4287c8b7d32e15e7df3e73f365409d7fe49a0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046524"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a>Eliminazione di utenti su server membri e Windows 2000 Professional

In questo argomento viene illustrato come eliminare un utente da un server membro o da un computer che esegue Windows 2000 Professional.

**Per eliminare un utente**

1.  Eseguire l'associazione al computer utilizzando le regole seguenti:
    1.  Utilizzare un account con diritti sufficienti per accedere a tale computer.
    2.  Usare il formato stringa di binding seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare a ADSI che è in associazione a un computer: "WinNT:// <computer name> <computer> ". Il &lt; parametro "nome computer &gt; " è il nome del computer di cui si desidera accedere ai gruppi. Questo parametro notifica a ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si sta effettuando l'associazione.
    3.  Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Specificare "User" come classe usando [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) per eliminare l'utente.

    Tenere presente che non è necessario chiamare [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) per eseguire il commit della modifica nel contenitore. La chiamata a [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) consente di eseguire il commit dell'eliminazione dell'utente direttamente nella directory.

 

 