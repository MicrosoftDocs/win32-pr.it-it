---
description: Se un Windows non dispone di un elenco di controllo di accesso discrezionale (DACL), il sistema consente l'accesso completo a tutti gli utenti.
ms.assetid: be9633fb-14ef-42d2-9269-84287b35b653
title: DACL e ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07bf87c2bd5f64b7178eca9d9fedd695a8b618430bf505f74be297780e48f774
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782181"
---
# <a name="dacls-and-aces"></a>DACL e ACE

Se un Windows non dispone di [](/windows/desktop/SecGloss/d-gly) un elenco di controllo di accesso discrezionale (DACL), il sistema consente l'accesso completo a tutti gli utenti. Se un oggetto dispone di un elenco DACL, il [](/windows/desktop/SecGloss/a-gly) sistema consente solo l'accesso consentito in modo esplicito dalle voci di controllo di accesso (ACE) nell'elenco DACL. Se non sono presenti ACE nell'elenco DACL, il sistema non consente l'accesso a nessuno. Analogamente, se un dacl dispone di ACE che consentono l'accesso a un set limitato di utenti o gruppi, il sistema nega implicitamente l'accesso a tutti i fiduciari non inclusi nelle ACE.

Nella maggior parte dei casi, è possibile controllare l'accesso a un oggetto usando le ACE consentite per l'accesso. Non è necessario negare in modo esplicito l'accesso a un oggetto . L'eccezione si verifica quando una ACE consente l'accesso a un gruppo e si vuole negare l'accesso a un membro del gruppo. A tale scopo, inserire una ACE con accesso negato per l'utente nell'elenco DACL prima della ACE consentita per il gruppo. Si noti che [l'ordine delle ACE](order-of-aces-in-a-dacl.md) è importante perché il sistema legge le voci ACE in sequenza fino a quando l'accesso non viene concesso o negato. La ACE negata dall'accesso dell'utente deve essere visualizzata per prima. in caso contrario, quando il sistema legge l'ACE consentita per l'accesso del gruppo, concederà l'accesso all'utente con restrizioni.

La figura seguente mostra un elenco DACL che nega l'accesso a un utente e concede l'accesso a due gruppi. I membri del gruppo A ottengono i diritti di accesso lettura, scrittura ed esecuzione accumulando i diritti consentiti al gruppo A e i diritti consentiti a Tutti. L'eccezione è Andrew, a cui viene negato l'accesso dalla ACE negata dall'accesso nonostante sia membro del gruppo Everyone.

![dacl che concede diritti di accesso diversi in base all'appartenenza ai gruppi](images/accctrl1.png)

 

 
