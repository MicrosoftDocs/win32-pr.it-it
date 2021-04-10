---
description: Per utilizzare la sicurezza basata sui ruoli nell'applicazione COM+, è necessario innanzitutto abilitare il controllo delle autorizzazioni in base al ruolo per l'applicazione.
ms.assetid: d391a0d4-fe5d-4587-b0b1-b3aa294b7ad7
title: Abilitazione del controllo dell'autorizzazione Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4268c35812af04ed8a0056900e821029274756
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049226"
---
# <a name="enabling-role-based-authorization-checking"></a>Abilitazione del controllo dell'autorizzazione Role-Based

Per utilizzare la sicurezza basata sui ruoli nell'applicazione COM+, è necessario innanzitutto abilitare il controllo delle autorizzazioni in base al ruolo per l'applicazione. In questo modo si garantisce che gli utenti che accedono all'applicazione vengano controllati per il ruolo a cui appartengono prima che siano autorizzati a eseguire qualsiasi operazione nell'applicazione. Se il controllo delle autorizzazioni in base al ruolo non è abilitato, la protezione basata sui ruoli per l'applicazione non viene utilizzata.

**Per abilitare il controllo dell'autorizzazione basata sui ruoli**

1.  Fare clic con il pulsante destro del mouse sull'applicazione COM+ per la quale si sta abilitando il controllo dell'autorizzazione basata sui ruoli, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .

3.  In **autorizzazione**, selezionare la casella **di controllo Imponi controlli di accesso per l'applicazione** . la cancellazione della casella di controllo indica che la sicurezza basata sui ruoli non viene utilizzata per l'applicazione.

4.  Fare clic su **OK**.

L'impostazione di autorizzazione selezionata verrà applicata al successivo avvio dell'applicazione.

 

 



