---
title: Creazione di utenti su server membri e Windows 2000 Professional
description: Questo argomento descrive i passaggi usati per creare un utente in un server membro o in un computer che esegue Windows 2000 Professional.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- Creazione di utenti su server membri e Windows 2000 Professional AD
- utenti AD, creazione di un utente su server membri e Windows 2000 Professional
- Active Directory, utilizzo di, utenti, creazione di un utente su server membri e Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050c9e8ecf68465097f2c185d2d31e0195c25a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046532"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a>Creazione di utenti su server membri e Windows 2000 Professional

**Per creare un utente**

1.  Eseguire l'associazione al computer utilizzando le regole seguenti:
    1.  Utilizzare un account con diritti sufficienti per accedere a tale computer.
    2.  Usare il formato stringa di binding seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare a ADSI che è in associazione a un computer: "WinNT:// <computer name> <computer> ". Il &lt; computer "nome computer &gt; " è il nome del computer di cui si desidera accedere ai gruppi. Questo parametro indica a ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si sta effettuando l'associazione.
    3.  Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Specificare "User" come classe usando [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) per aggiungere l'utente.
3.  Scrivere l'utente nel database di sicurezza del computer utilizzando [**IADs. seinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 