---
title: Enumerazione degli utenti nei server membri e Windows 2000 Professional
description: Questo argomento illustra come enumerare tutti gli utenti, in un database di sicurezza locale, nei server membri e nei computer in Windows 2000 Professional.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- Enumerazione degli utenti nei server membri e Windows 2000 Professional AD
- users AD , Enumerazione degli utenti nei server membri e Windows 2000 Professional
- Active Directory, uso, utenti, enumerazione degli utenti nei server membri e Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f72e38a00e0fcc4310f7b8498b0dda28d71231df7e65fcf2de9945f5feef2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694878"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a>Enumerazione degli utenti nei server membri e Windows 2000 Professional

Questo argomento illustra come enumerare tutti gli utenti, in un database di sicurezza locale, nei server membri e nei computer in Windows 2000 Professional.

**Per enumerare gli utenti**

1.  Eseguire l'associazione al computer usando le regole seguenti:
    1.  Usare un account con diritti sufficienti per accedere al computer.
    2.  Usare il formato di stringa di associazione seguente usando il provider WinNT, il nome del computer e un parametro aggiuntivo per indicare ad ADSI che è l'associazione a un computer: "WinNT:// <computer name> , <computer> ". Il parametro " computer name " è il nome del computer a &lt; &gt; cui accedere ai gruppi. Questo parametro indica ad ADSI che è associato a un computer e consente al parser del provider WinNT di ignorare alcune query di risoluzione dell'ambiguità per determinare il tipo di oggetto a cui si esegue l'associazione.
    3.  Eseguire l'associazione [**all'interfaccia IADsContainer.**](/windows/desktop/api/iads/nn-iads-iadscontainer)
2.  Aggiungere "user" alla [**proprietà IADsContainer.Filter.**](/windows/desktop/ADSI/iadscontainer-property-methods) In questo modo l'enumerazione contiene solo oggetti con la classe di oggetti "user".
3.  Enumerare gli oggetti . Per ogni oggetto utente, usare i [**metodi dell'interfaccia IADs**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) per leggere le proprietà dell'utente.

 

 