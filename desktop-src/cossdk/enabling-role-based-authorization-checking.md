---
description: Per usare la sicurezza basata sui ruoli nell'applicazione COM+, è innanzitutto necessario abilitare il controllo delle autorizzazioni in base al ruolo per l'applicazione.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Abilitazione Role-Based di autorizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd46a0b09b981a3dd7731f5839458550379dad5619f22d1caaaddb24e87deaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813859"
---
# <a name="enabling-role-based-authorization-checking"></a>Abilitazione Role-Based di autorizzazione

Per usare la sicurezza basata sui ruoli nell'applicazione COM+, è innanzitutto necessario abilitare il controllo delle autorizzazioni in base al ruolo per l'applicazione. In questo modo si garantisce che agli utenti che accedono all'applicazione venga verificato il ruolo a cui appartengono prima di essere autorizzati a eseguire qualsiasi operazione nell'applicazione. Se il controllo delle autorizzazioni in base al ruolo non è abilitato, la sicurezza basata sui ruoli per l'applicazione non viene utilizzata.

**Per abilitare il controllo delle autorizzazioni in base al ruolo**

1.  Fare clic con il pulsante destro del mouse sull'applicazione COM+ per cui si sta abilitando il controllo delle autorizzazioni basate sui ruoli e quindi **scegliere Proprietà.**

2.  Nella finestra di dialogo delle proprietà dell'applicazione fare clic **sulla scheda** Sicurezza .

3.  In **Autorizzazione** selezionare la casella **di controllo Imponi controlli di accesso** per questa applicazione. Se si deseleziona la casella di controllo, la sicurezza basata sui ruoli non viene utilizzata per l'applicazione.

4.  Fare clic su **OK**.

L'impostazione di autorizzazione selezionata viene attivata al successivo avvio dell'applicazione.

 

 



