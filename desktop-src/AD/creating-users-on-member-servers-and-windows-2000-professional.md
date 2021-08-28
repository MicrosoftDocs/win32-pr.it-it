---
title: Creazione di utenti nei server membri e Windows 2000 Professional
description: Questo argomento descrive i passaggi usati per creare un utente in un server membro o in un computer che esegue Windows 2000 Professional.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- Creazione di utenti nei server membri e Windows 2000 Professional AD
- users AD , creazione di un utente nei server membri e Windows 2000 Professional
- Active Directory, uso, utenti, creazione di un utente nei server membri e Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21490302b025e20f836cbbc957d0f86824b3456d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881576"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a>Creazione di utenti nei server membri e Windows 2000 Professional

**Per creare un utente**

1.  Eseguire l'associazione al computer usando le regole seguenti:
    1.  Usare un account con diritti sufficienti per accedere al computer.
    2.  Usare il formato di stringa di associazione seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare ad ADSI che è in associazione a un computer: "WinNT:// <computer name> , &lt; computer &gt; ". Il " nome computer " computer è il nome del computer di cui si vuole accedere &lt; &gt; ai gruppi. Questo parametro indica ad ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si esegue l'associazione.
    3.  Eseguire l'associazione [**all'interfaccia IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)
2.  Specificare "user" come classe usando [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) per aggiungere l'utente.
3.  Scrivere l'utente nel database di sicurezza del computer [**usando IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 
