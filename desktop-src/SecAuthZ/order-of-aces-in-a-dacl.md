---
description: Quando un processo tenta di accedere a un oggetto a protezione diretta, il sistema scorre le voci di controllo di accesso (ACE) nell'elenco di controllo di accesso discrezionale (DACL) degli oggetti fino a quando non trova le voci ACE che consentono o negano l'accesso richiesto.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Ordine delle voci ACE in un DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc45d6fd286bb06bd4311a8a02010c68832735ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314729"
---
# <a name="order-of-aces-in-a-dacl"></a>Ordine delle voci ACE in un DACL

Quando un [*processo*](/windows/desktop/SecGloss/p-gly) tenta di accedere a un oggetto a protezione diretta, il sistema scorre le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) nell' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) dell'oggetto fino a trovare le voci ACE che consentono o negano l'accesso richiesto. I diritti di accesso consentiti a un elenco DACL possono variare a seconda dell'ordine delle voci ACE nell'elenco DACL. Di conseguenza, il sistema operativo Windows XP definisce un ordine preferito per le voci ACE nell'elenco DACL di un oggetto a protezione diretta. L'ordine preferito fornisce un semplice Framework che garantisce che una voce ACE con accesso negato neghi effettivamente l'accesso. Per ulteriori informazioni sull'algoritmo del sistema per il controllo dell'accesso, vedere [come gli elenchi DACL controllano l'accesso a un oggetto](how-dacls-control-access-to-an-object.md).

Per Windows Server 2003 e Windows XP, l'ordine corretto degli ACE è complicato dall'introduzione delle voci ACE specifiche dell'oggetto e dell'ereditarietà automatica.

Nei passaggi seguenti viene descritto l'ordine preferito:

1.  Tutte le voci ACE esplicite vengono inserite in un gruppo prima di eventuali ACE ereditate.
2.  All'interno del gruppo di voci ACE esplicite, le voci ACE con accesso negato vengono inserite prima degli ACE consentiti per l'accesso.
3.  Le voci ACE ereditate vengono inserite nell'ordine in cui vengono ereditate. Le voci ACE ereditate dall'elemento padre dell'oggetto figlio vengono prima di tutto, quindi le voci ACE ereditate dal padre e così via fino all'albero degli oggetti.
4.  Per ogni livello di ACE ereditate, le voci ACE con accesso negato vengono inserite prima degli ACE consentiti per l'accesso.

Naturalmente, non tutti i tipi ACE sono necessari in un ACL.

Funzioni quali [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) e [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) aggiungono una voce ACE alla fine di un ACL. È responsabilità del chiamante assicurarsi che le voci ACE vengano aggiunte nell'ordine corretto.

 

 
