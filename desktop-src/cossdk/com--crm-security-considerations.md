---
description: Considerazioni sulla sicurezza di COM+ CRM
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Considerazioni sulla sicurezza di COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ababde9f31c0c2655fbf4f0c46b216ca0cbfee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126357"
---
# <a name="com-crm-security-considerations"></a><span data-ttu-id="877a8-103">Considerazioni sulla sicurezza di COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="877a8-103">COM+ CRM Security Considerations</span></span>

<span data-ttu-id="877a8-104">Un file di log CRM potrebbe contenere informazioni riservate che devono essere protette.</span><span class="sxs-lookup"><span data-stu-id="877a8-104">A CRM log file could contain sensitive information that must be secured.</span></span> <span data-ttu-id="877a8-105">Per questo motivo, se l'applicazione server viene eseguita con una qualsiasi identità diversa dall'utente interattivo quando viene creato per la prima volta il file di log CRM, il file di log CRM è protetto dalla sicurezza solo per tale utente.</span><span class="sxs-lookup"><span data-stu-id="877a8-105">For this reason, if the server application is running under any identity other than Interactive User when the CRM log file is first created, the CRM log file is security protected for that user only.</span></span> <span data-ttu-id="877a8-106">Questa funzionalità è disponibile solo nel file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="877a8-106">This feature is available only on the NTFS file system.</span></span> <span data-ttu-id="877a8-107">Se successivamente si modifica l'identità dell'applicazione server, le informazioni di sicurezza per il file di log CRM non vengono modificate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="877a8-107">If the identity of the server application is subsequently changed, the security information for the CRM log file is not automatically changed.</span></span> <span data-ttu-id="877a8-108">Può essere modificato manualmente usando gli strumenti di amministrazione di Windows esistenti.</span><span class="sxs-lookup"><span data-stu-id="877a8-108">It can be changed manually by using existing Windows administration tools.</span></span> <span data-ttu-id="877a8-109">L'alternativa consiste semplicemente nell'eliminare il file di log CRM quando si trova in uno stato pulito, che è previsto dopo un arresto controllato dell'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="877a8-109">The alternative is simply to delete the CRM log file when it is in a clean state (which is expected after a controlled shutdown of the server application).</span></span>

<span data-ttu-id="877a8-110">Nel normale funzionamento, COM+ crea il componente di compensazione CRM e chiama l'interfaccia [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) .</span><span class="sxs-lookup"><span data-stu-id="877a8-110">In normal operation, COM+ creates the CRM compensator component and calls the [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) interface.</span></span> <span data-ttu-id="877a8-111">Tuttavia, un utente che dispone dei privilegi per creare il compensatore CRM può chiamare l'interfaccia **ICrmCompensator** in momenti inappropriati, causando possibili problemi di sicurezza del sistema.</span><span class="sxs-lookup"><span data-stu-id="877a8-111">However, a user having privileges to create the CRM Compensator can call the **ICrmCompensator** interface at inappropriate times, possibly causing system security problems.</span></span> <span data-ttu-id="877a8-112">Per garantire la protezione da questi problemi di sicurezza, l'amministratore di sistema può utilizzare la protezione basata sui ruoli per limitare il componente di compensazione CRM solo alle identità delle applicazioni server in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="877a8-112">To help protect against these security problems, the system administrator can use role-based security to restrict the CRM Compensator component to only those identities of the server applications in which it runs.</span></span> <span data-ttu-id="877a8-113">Se il componente è in esecuzione in un'applicazione di libreria, sono incluse tutte le identità delle applicazioni server.</span><span class="sxs-lookup"><span data-stu-id="877a8-113">If the component is running in a library application, this would include all the identities of the server applications.</span></span>

> [!Note]  
> <span data-ttu-id="877a8-114">A partire da Windows Server 2003, per impedire l'attivazione dall'esterno dell'applicazione server, è possibile garantire un sistema più sicuro contrassegnando il componente CRM Compensator come privato.</span><span class="sxs-lookup"><span data-stu-id="877a8-114">Starting with Windows Server 2003, to help prevent activation from outside the server application, it is possible to further ensure a more secure system by marking the CRM Compensator component as private.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="877a8-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="877a8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="877a8-116">Concetti Gestione risorse di compensazione COM+</span><span class="sxs-lookup"><span data-stu-id="877a8-116">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



