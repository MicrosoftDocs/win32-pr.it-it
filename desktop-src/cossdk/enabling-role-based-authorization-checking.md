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
# <a name="enabling-role-based-authorization-checking"></a><span data-ttu-id="b703d-103">Abilitazione del controllo dell'autorizzazione Role-Based</span><span class="sxs-lookup"><span data-stu-id="b703d-103">Enabling Role-Based Authorization Checking</span></span>

<span data-ttu-id="b703d-104">Per utilizzare la sicurezza basata sui ruoli nell'applicazione COM+, è necessario innanzitutto abilitare il controllo delle autorizzazioni in base al ruolo per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b703d-104">To use role-based security in your COM+ application, you must first enable role-based authorization checking for the application.</span></span> <span data-ttu-id="b703d-105">In questo modo si garantisce che gli utenti che accedono all'applicazione vengano controllati per il ruolo a cui appartengono prima che siano autorizzati a eseguire qualsiasi operazione nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b703d-105">This ensures that users who are accessing the application are checked for the role they belong to before they are authorized to do anything in the application.</span></span> <span data-ttu-id="b703d-106">Se il controllo delle autorizzazioni in base al ruolo non è abilitato, la protezione basata sui ruoli per l'applicazione non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b703d-106">If role-based authorization checking is not enabled, role-based security for the application is not used.</span></span>

<span data-ttu-id="b703d-107">**Per abilitare il controllo dell'autorizzazione basata sui ruoli**</span><span class="sxs-lookup"><span data-stu-id="b703d-107">**To enable role-based authorization checking**</span></span>

1.  <span data-ttu-id="b703d-108">Fare clic con il pulsante destro del mouse sull'applicazione COM+ per la quale si sta abilitando il controllo dell'autorizzazione basata sui ruoli, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="b703d-108">Right-click the COM+ application for which you are enabling role-based authorization checking, and then click **Properties**.</span></span>

2.  <span data-ttu-id="b703d-109">Nella finestra di dialogo Proprietà applicazione fare clic sulla scheda **sicurezza** .</span><span class="sxs-lookup"><span data-stu-id="b703d-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="b703d-110">In **autorizzazione**, selezionare la casella **di controllo Imponi controlli di accesso per l'applicazione** . la cancellazione della casella di controllo indica che la sicurezza basata sui ruoli non viene utilizzata per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b703d-110">Under **Authorization**, select the **Enforce access checks for this application** check box; clearing the check box means that role-based security is not used for the application.</span></span>

4.  <span data-ttu-id="b703d-111">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="b703d-111">Click **OK**.</span></span>

<span data-ttu-id="b703d-112">L'impostazione di autorizzazione selezionata verrà applicata al successivo avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b703d-112">The selected authorization setting takes effect the next time the application is started.</span></span>

 

 



