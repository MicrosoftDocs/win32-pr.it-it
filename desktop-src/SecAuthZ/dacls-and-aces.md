---
description: Se un oggetto Windows non dispone di un elenco di controllo di accesso discrezionale (DACL), il sistema consente a tutti gli utenti di accedervi.
ms.assetid: be9633fb-14ef-42d2-9269-84287b35b653
title: Elenchi DACL e ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28bf351fd59f634a7c7bf960aedac1c76659ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233699"
---
# <a name="dacls-and-aces"></a>Elenchi DACL e ACE

Se un oggetto Windows non dispone di un [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL), il sistema consente a tutti gli utenti di accedervi. Se un oggetto dispone di un DACL, il sistema consente solo l'accesso consentito in modo esplicito dalle [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) nell'elenco DACL. Se non sono presenti voci ACE nell'elenco DACL, il sistema non consente l'accesso a nessuno. Analogamente, se un elenco DACL include ACE che consentono l'accesso a un set limitato di utenti o gruppi, il sistema nega in modo implicito l'accesso a tutti i trustee non inclusi nelle voci ACE.

Nella maggior parte dei casi, è possibile controllare l'accesso a un oggetto usando le voci di accesso consentito. non è necessario negare esplicitamente l'accesso a un oggetto. L'eccezione si verifica quando una voce ACE consente l'accesso a un gruppo e si vuole negare l'accesso a un membro del gruppo. A tale scopo, inserire una voce ACE di accesso negato per l'utente nell'elenco DACL in anticipo rispetto all'ACE consentito per l'accesso per il gruppo. Si noti che l' [ordine delle voci ACE](order-of-aces-in-a-dacl.md) è importante perché il sistema legge le voci ACE in sequenza fino a quando l'accesso non viene concesso o negato. La voce ACE di accesso negato dell'utente deve essere visualizzata per prima. in caso contrario, quando il sistema legge l'ACE consentito per l'accesso al gruppo, consentirà l'accesso all'utente con restrizioni.

Nella figura seguente viene illustrato un DACL che nega l'accesso a un utente e concede l'accesso a due gruppi. I membri del gruppo A ottengono i diritti di accesso di lettura, scrittura ed esecuzione accumulando i diritti consentiti per raggruppare un e i diritti consentiti a tutti. L'eccezione è Andrew, a cui viene negato l'accesso dalla voce ACE di accesso negato, nonostante sia un membro del gruppo Everyone.

![DACL che concede diritti di accesso diversi in base all'appartenenza al gruppo](images/accctrl1.png)

 

 
