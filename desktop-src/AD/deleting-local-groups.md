---
title: Eliminazione di gruppi locali
description: In questo argomento viene illustrato come eliminare un gruppo locale da un server membro o da un computer in esecuzione Windows 2000 Professional.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Eliminazione dei gruppi locali ad Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe960804e083ecaf8ef12e412a43b7b8db4800f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881479"
---
# <a name="deleting-local-groups"></a>Eliminazione di gruppi locali

In questo argomento viene illustrato come eliminare un gruppo locale da un server membro o da un computer in esecuzione Windows 2000 Professional.

**Per eliminare un gruppo locale**

1.  Eseguire il binding al computer usando le regole seguenti:
    1.  Usare un account con diritti sufficienti per accedere al computer.
    2.  Usare il formato di stringa di associazione seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare ad ADSI che è in associazione a un computer: "WinNT:// <computer name> , &lt; computer &gt; ". Il parametro " &lt; nome computer " è il nome del gruppo di computer a cui &gt; accedere. Questo parametro indica ad ADSI che è in fase di associazione a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si esegue l'associazione.
    3.  Eseguire il binding [**all'interfaccia IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)
2.  Specificare "group" come classe usando [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)per eliminare il gruppo.

    Non è necessario chiamare [**IADs.SetInfo per**](/windows/desktop/api/iads/nf-iads-iads-setinfo) eseguire il commit della modifica nel contenitore. La [**chiamata IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) esegue il commit dell'eliminazione del gruppo direttamente nella directory.

 

 
