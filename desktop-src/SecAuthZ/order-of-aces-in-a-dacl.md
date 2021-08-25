---
description: Quando un processo tenta di accedere a un oggetto a protezione diretta, il sistema passa attraverso le voci di controllo di accesso (ACE) nell'elenco di controllo di accesso discrezionale (DACL) degli oggetti fino a trovare le voci ACE che consentono o negano l'accesso richiesto.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Ordine delle voci ACE in un elenco DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b5d017fe6441e90cded6458d8796dee301e3fa0fda01b7d088039abd9834ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907751"
---
# <a name="order-of-aces-in-a-dacl"></a>Ordine delle voci ACE in un elenco DACL

Quando [](/windows/desktop/SecGloss/p-gly) un processo tenta di accedere a un oggetto a protezione diretta, il sistema passa attraverso le voci di controllo di accesso [](/windows/desktop/SecGloss/a-gly) (ACE) nell'elenco di controllo di accesso discrezionale [](/windows/desktop/SecGloss/d-gly) (DACL) dell'oggetto finché non trova le voci ACE che consentono o negano l'accesso richiesto. I diritti di accesso che un elenco DACL consente a un utente possono variare a seconda dell'ordine delle voci ACE nell'elenco DACL. Di conseguenza, il Windows sistema operativo XP definisce un ordine preferito per le voci ACE nell'elenco DACL di un oggetto a protezione diretta. L'ordine preferito fornisce un framework semplice che garantisce che una ACE nega effettivamente l'accesso. Per altre informazioni sull'algoritmo del sistema per il controllo dell'accesso, vedere [Come daCL controllano l'accesso a un oggetto](how-dacls-control-access-to-an-object.md).

Per Windows Server 2003 e Windows XP, l'ordine corretto delle ACE è complicato dall'introduzione di ACE specifiche dell'oggetto e dell'ereditarietà automatica.

La procedura seguente descrive l'ordine preferito:

1.  Tutte le ACE esplicite vengono inserite in un gruppo prima di qualsiasi ACE ereditata.
2.  All'interno del gruppo di ACE esplicite, le voci ACE negate di accesso vengono inserite prima delle ACE consentite per l'accesso.
3.  Le voci ACE ereditate vengono inserite nell'ordine in cui vengono ereditate. Le voci ACE ereditate dall'oggetto padre dell'oggetto figlio vengono prima di tutto, quindi le ACE ereditate dal nonno e così via nell'albero degli oggetti.
4.  Per ogni livello di ACE ereditate, le ACE negate di accesso vengono inserite prima delle ACE consentite per l'accesso.

Naturalmente, non tutti i tipi ACE sono necessari in un elenco di controllo di accesso.

Funzioni come [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) e [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) aggiungono una ACE alla fine di un ACL. È responsabilità del chiamante assicurarsi che le voci ACE siano aggiunte nell'ordine corretto.

 

 
