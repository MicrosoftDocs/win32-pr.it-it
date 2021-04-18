---
description: Alcune funzioni richiedono privilegi speciali per una corretta esecuzione.
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: Esecuzione con privilegi speciali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be662d187ef27c7afc12b031f2d8de225d34c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318248"
---
# <a name="running-with-special-privileges"></a><span data-ttu-id="3570d-103">Esecuzione con privilegi speciali</span><span class="sxs-lookup"><span data-stu-id="3570d-103">Running with Special Privileges</span></span>

<span data-ttu-id="3570d-104">Alcune funzioni richiedono [privilegi](/windows/desktop/SecAuthZ/privileges) speciali per una corretta esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3570d-104">Some functions require special [privileges](/windows/desktop/SecAuthZ/privileges) to run correctly.</span></span> <span data-ttu-id="3570d-105">In alcuni casi, la funzione può essere eseguita solo da determinati utenti o da membri di determinati gruppi.</span><span class="sxs-lookup"><span data-stu-id="3570d-105">In some cases, the function can only be run by certain users or by members of certain groups.</span></span> <span data-ttu-id="3570d-106">Il requisito più comune è che l'utente sia un amministratore locale.</span><span class="sxs-lookup"><span data-stu-id="3570d-106">The most common requirement is that the user be a local administrator.</span></span> <span data-ttu-id="3570d-107">Per altre funzioni è necessario che l'account dell'utente disponga di privilegi specifici abilitati.</span><span class="sxs-lookup"><span data-stu-id="3570d-107">Other functions require the user's account to have specific privileges enabled.</span></span>

<span data-ttu-id="3570d-108">Per ridurre la possibilità che il codice non autorizzato possa ottenere il controllo, il sistema deve essere eseguito con il privilegio minimo necessario.</span><span class="sxs-lookup"><span data-stu-id="3570d-108">To reduce the possibility of unauthorized code being able to get control, the system should run with the least privilege necessary.</span></span> <span data-ttu-id="3570d-109">Le applicazioni che devono chiamare funzioni che richiedono privilegi speciali possono lasciare il sistema aperto per attaccare gli hacker.</span><span class="sxs-lookup"><span data-stu-id="3570d-109">Applications that need to call functions that require special privileges can leave the system open to attack by hackers.</span></span> <span data-ttu-id="3570d-110">Tali applicazioni devono essere progettate per essere eseguite per brevi periodi di tempo e informare l'utente delle implicazioni di sicurezza implicate.</span><span class="sxs-lookup"><span data-stu-id="3570d-110">Such applications should be designed to run for short periods of time and should inform the user of the security implications involved.</span></span>

<span data-ttu-id="3570d-111">Per informazioni sull'esecuzione di come utenti diversi e su come abilitare i privilegi nell'applicazione, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="3570d-111">For information about how to run as different users and how to enable privileges in your application, see the following topics:</span></span><dl>

[<span data-ttu-id="3570d-112">Esecuzione con privilegi di amministratore</span><span class="sxs-lookup"><span data-stu-id="3570d-112">Running with Administrator Privileges</span></span>](running-with-administrator-privileges.md)  
[<span data-ttu-id="3570d-113">Chiedere all'utente le credenziali</span><span class="sxs-lookup"><span data-stu-id="3570d-113">Asking the User for Credentials</span></span>](asking-the-user-for-credentials.md)  
[<span data-ttu-id="3570d-114">Modifica dei privilegi in un token</span><span class="sxs-lookup"><span data-stu-id="3570d-114">Changing Privileges in a Token</span></span>](changing-privileges-in-a-token.md)  
[<span data-ttu-id="3570d-115">Assegnazione di privilegi a un account</span><span class="sxs-lookup"><span data-stu-id="3570d-115">Assigning Privileges to an Account</span></span>](assigning-privileges-to-an-account.md)  
</dl>

 

 
