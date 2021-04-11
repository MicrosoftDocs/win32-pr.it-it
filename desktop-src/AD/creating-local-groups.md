---
title: Creazione di gruppi locali
description: Per i server membri e Windows 2000 Professional è possibile creare solo gruppi locali.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Creazione di gruppi locali AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705902b0066913fcd6eed56ba7c74e299144595f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336814"
---
# <a name="creating-local-groups"></a>Creazione di gruppi locali

Per i server membri e Windows 2000 Professional è possibile creare solo gruppi locali.

**Per creare un gruppo locale per un server membro o un computer che esegue Windows 2000 Professional**

1.  Eseguire l'associazione al computer utilizzando le regole seguenti:
    1.  Utilizzare un account con diritti sufficienti per accedere a tale computer.
    2.  Usare il formato stringa di binding seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare a ADSI che è in associazione a un computer: "WinNT:// <computer name> <computer> ".

        Il &lt; parametro "nome computer &gt; " è il nome dei gruppi di computer a cui accedere.

        Nella stringa di binding il parametro " &lt; computer &gt; " indica a ADSI che è associato a un computer. ADSI rende questi dati disponibili per il parser del provider WinNT in modo che possa ignorare alcune query di risoluzione ambiguità per determinare il tipo di oggetto a cui si sta effettuando l'associazione.

    3.  Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .

2.  Specificare "localGroup" come classe usando [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) per aggiungere il gruppo.
    > [!Note]  
    > Se si specifica "Group" come classe, ADSI USA "localGroup". Non specificare la classe come "globalGroup". Non è possibile creare gruppi della classe "globalGroup" nei server membro o in un computer che esegue Windows NT Workstation/Windows 2000 Professional. Se si specifica "globalGroup", [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) crea il gruppo nella cache delle proprietà, ma [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) non scrive il gruppo nel database di sicurezza e non restituisce un errore.

     

3.  Scrivere il gruppo nel database di sicurezza del computer utilizzando [**IADs. seinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 