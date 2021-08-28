---
title: Creazione di gruppi locali
description: È possibile creare solo gruppi locali per i server membri e Windows 2000 Professional.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Creazione di gruppi locali AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06410572e6e5897280b2a03c99b387dbf81b3cca
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881585"
---
# <a name="creating-local-groups"></a>Creazione di gruppi locali

È possibile creare solo gruppi locali per i server membri e Windows 2000 Professional.

**Per creare un gruppo locale per un server membro o un computer che esegue Windows 2000 Professional**

1.  Eseguire il binding al computer usando le regole seguenti:
    1.  Usare un account con diritti sufficienti per accedere al computer.
    2.  Usare il formato di stringa di associazione seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare ad ADSI che è in associazione a un computer: "WinNT:// <computer name> , &lt; computer &gt; ".

        Il parametro " &lt; nome computer " è il nome dei gruppi di computer a cui &gt; accedere.

        Nella stringa di associazione il parametro " computer " indica ad ADSI che &lt; è in associazione a un &gt; computer. ADSI rende disponibili questi dati al parser del provider WinNT in modo che possa ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si esegue l'associazione.

    3.  Eseguire il binding [**all'interfaccia IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)

2.  Specificare "localGroup" come classe usando [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) per aggiungere il gruppo.
    > [!Note]  
    > Se si specifica "group" come classe, ADSI usa "localGroup". Non specificare la classe come "globalGroup". Non è possibile creare gruppi della classe "globalGroup" nei server membri o in un computer che esegue Windows NT Workstation/Windows 2000 Professional. Se si specifica "globalGroup", [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) crea il gruppo nella cache delle proprietà, ma [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) non scrive il gruppo nel database di sicurezza e non restituisce un errore.

     

3.  Scrivere il gruppo nel database di sicurezza del computer [**usando IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 
