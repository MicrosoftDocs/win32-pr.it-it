---
title: Enumerazione degli utenti su server membri e Windows 2000 Professional
description: In questo argomento viene illustrato come enumerare tutti gli utenti, in un database di sicurezza locale, su server membri e computer che eseguono Windows 2000 Professional.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- Enumerazione degli utenti su server membri e Windows 2000 Professional AD
- utenti AD, enumerazione di utenti su server membri e Windows 2000 Professional
- Active Directory, utilizzo di, utenti, enumerazione di utenti su server membri e Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664af51b7feb2e0b9a683664659eefda11c9cb9d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724551"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a>Enumerazione degli utenti su server membri e Windows 2000 Professional

In questo argomento viene illustrato come enumerare tutti gli utenti, in un database di sicurezza locale, su server membri e computer che eseguono Windows 2000 Professional.

**Per enumerare gli utenti**

1.  Eseguire l'associazione al computer utilizzando le regole seguenti:
    1.  Utilizzare un account con diritti sufficienti per accedere a tale computer.
    2.  Usare il formato stringa di binding seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare a ADSI che è in associazione a un computer: "WinNT:// <computer name> <computer> ". Il &lt; parametro "nome computer &gt; " è il nome del computer per cui si desidera accedere ai gruppi. Questo parametro indica a ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si sta effettuando l'associazione.
    3.  Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Aggiungere "User" alla proprietà [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) . In questo modo l'enumerazione conterrà solo oggetti con la classe di oggetti "User".
3.  Enumerare gli oggetti. Per ogni oggetto utente, usare i metodi di interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) per leggere le proprietà utente.

 

 