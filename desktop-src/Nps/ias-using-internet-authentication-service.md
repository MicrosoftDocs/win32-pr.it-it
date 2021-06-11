---
title: Uso delle estensioni di Server dei criteri di rete
description: Informazioni sull'uso delle estensioni NPS. Il servizio Autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete.
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- Internet Authentication Service IAS , attività
- Internet Authentication Service IAS , con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f422c005d6810a4035450e24de1324b28361f1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989071"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="3c549-106">Uso delle estensioni di Server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="3c549-106">Using NPS Extensions</span></span>

<span data-ttu-id="3c549-107">Il servizio Autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="3c549-107">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="3c549-108">Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="3c549-108">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="3c549-109">In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente denominate IAS.</span><span class="sxs-lookup"><span data-stu-id="3c549-109">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="3c549-110">\*\*Windows Server 2008 R2 e Windows Server 2008: \*\*</span><span class="sxs-lookup"><span data-stu-id="3c549-110">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="3c549-111">Gli esempi DialIn e MapName estendono la funzionalità NPS.</span><span class="sxs-lookup"><span data-stu-id="3c549-111">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="3c549-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="3c549-112">Sample</span></span>             | <span data-ttu-id="3c549-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c549-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c549-114">DialIn</span><span class="sxs-lookup"><span data-stu-id="3c549-114">DialIn</span></span><br/>  | <span data-ttu-id="3c549-115">Questo esempio implementa una DLL di estensione RADIUS che controlla il bit di accesso remoto per l'utente.</span><span class="sxs-lookup"><span data-stu-id="3c549-115">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="3c549-116">MapName</span><span class="sxs-lookup"><span data-stu-id="3c549-116">MapName</span></span><br/> | <span data-ttu-id="3c549-117">Questa DLL di estensione di esempio cerca l'account designato in tutti i domini attendibili.</span><span class="sxs-lookup"><span data-stu-id="3c549-117">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="3c549-118">Ciò consente agli utenti di più domini di essere autenticati senza che gli utenti devono specificare il proprio nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="3c549-118">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="3c549-119">Il codice sorgente per le applicazioni di esempio MapName e DialIn è riportato nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="3c549-119">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="3c549-120">*Percorso*, %Percorso di installazione%, indica la directory di installazione di base per i computer x64.</span><span class="sxs-lookup"><span data-stu-id="3c549-120">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="3c549-121">Vedere anche [Windows Software Development Kit (Windows SDK) (SDK) per Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (Windows SDK) (SDK) e Download per lo sviluppo di app di Windows [Store](https://msdn.microsoft.com/windows/apps/br229516).</span><span class="sxs-lookup"><span data-stu-id="3c549-121">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="3c549-122">Windows SDK per Windows 8</span><span class="sxs-lookup"><span data-stu-id="3c549-122">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="3c549-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3c549-123">Windows Server 2012</span></span>

<span data-ttu-id="3c549-124">Collegamento di download: N/D</span><span class="sxs-lookup"><span data-stu-id="3c549-124">Download link: N/A</span></span>

<span data-ttu-id="3c549-125">MapName: No</span><span class="sxs-lookup"><span data-stu-id="3c549-125">MapName: No</span></span>

<span data-ttu-id="3c549-126">DialIn: No</span><span class="sxs-lookup"><span data-stu-id="3c549-126">DialIn: No</span></span>

<span data-ttu-id="3c549-127">Località: N/D</span><span class="sxs-lookup"><span data-stu-id="3c549-127">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="3c549-128">Microsoft Windows Software Development Kit (Windows SDK) (SDK) per Windows 7 e .NET Framework 4.0</span><span class="sxs-lookup"><span data-stu-id="3c549-128">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="3c549-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3c549-129">Windows Server 2008 R2</span></span>

<span data-ttu-id="3c549-130">Collegamento di download: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="3c549-130">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="3c549-131">MapName: Sì</span><span class="sxs-lookup"><span data-stu-id="3c549-131">MapName: Yes</span></span>

<span data-ttu-id="3c549-132">DialIn: No</span><span class="sxs-lookup"><span data-stu-id="3c549-132">DialIn: No</span></span>

<span data-ttu-id="3c549-133">Percorso: %Install Path% \\ Microsoft SDKs \\ Windows \\ v7.1 \\ Samples \\ netds \\ ias</span><span class="sxs-lookup"><span data-stu-id="3c549-133">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="3c549-134">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="3c549-134">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="3c549-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c549-135">Windows Server 2008</span></span>

<span data-ttu-id="3c549-136">Collegamento di download: <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="3c549-136">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="3c549-137">MapName: Sì</span><span class="sxs-lookup"><span data-stu-id="3c549-137">MapName: Yes</span></span>

<span data-ttu-id="3c549-138">DialIn: No</span><span class="sxs-lookup"><span data-stu-id="3c549-138">DialIn: No</span></span>

<span data-ttu-id="3c549-139">Percorso: %Install Path% \\ Microsoft SDKs \\ Windows \\ v6.1 \\ Samples \\ NetDs \\ IAS</span><span class="sxs-lookup"><span data-stu-id="3c549-139">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="3c549-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c549-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c549-141">Download per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="3c549-141">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="3c549-142">Windows SDK per Windows 8</span><span class="sxs-lookup"><span data-stu-id="3c549-142">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





