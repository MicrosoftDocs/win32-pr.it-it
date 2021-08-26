---
title: Eliminazione di utenti nei server membri Windows 2000 Professional
description: Questo argomento illustra come eliminare un utente da un server membro o da un computer in esecuzione Windows 2000 Professional.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- users AD , eliminazione di un utente nei server membri Windows 2000 Professional
- Active Directory, uso, utenti, eliminazione di utenti nei server membri e Windows 2000 Professional
- eliminazione di un utente
- server, eliminazione di un utente
- eliminazione di utenti in server membri e Windows 2000 Professional AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e366356696c1e8b11a53b45aae3860600fc6555
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881447"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a>Eliminazione di utenti nei server membri Windows 2000 Professional

Questo argomento illustra come eliminare un utente da un server membro o da un computer in esecuzione Windows 2000 Professional.

**Per eliminare un utente**

1.  Eseguire l'associazione al computer usando le regole seguenti:
    1.  Usare un account con diritti sufficienti per accedere al computer.
    2.  Usare il formato di stringa di associazione seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare ad ADSI che è in associazione a un computer: "WinNT:// <computer name> , &lt; computer &gt; ". Il parametro " nome computer " è il nome del computer a cui si vuole accedere &lt; &gt; ai gruppi. Questo parametro notifica ad ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si esegue l'associazione.
    3.  Eseguire l'associazione [**all'interfaccia IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)
2.  Specificare "user" come classe usando [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) per eliminare l'utente.

    Tenere presente che non è necessario chiamare [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) per eseguire il commit della modifica nel contenitore. La [**chiamata IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) esegue il commit dell'eliminazione dell'utente direttamente nella directory.

 

 
