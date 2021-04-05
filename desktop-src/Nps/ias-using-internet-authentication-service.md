---
title: Uso delle estensioni NPS
description: Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- IAS servizio di autenticazione Internet, attività
- IAS servizio di autenticazione Internet, utilizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cc9f10c810ec9fe16618144db11686a1e2132
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104516681"
---
# <a name="using-nps-extensions"></a><span data-ttu-id="b11ff-105">Uso delle estensioni NPS</span><span class="sxs-lookup"><span data-stu-id="b11ff-105">Using NPS Extensions</span></span>

<span data-ttu-id="b11ff-106">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS).</span><span class="sxs-lookup"><span data-stu-id="b11ff-106">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span> <span data-ttu-id="b11ff-107">Il contenuto di questo argomento si applica sia a IAS che a NPS.</span><span class="sxs-lookup"><span data-stu-id="b11ff-107">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="b11ff-108">In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.</span><span class="sxs-lookup"><span data-stu-id="b11ff-108">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

<span data-ttu-id="b11ff-109">\* \* Windows Server 2008 R2 e Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="b11ff-109">\*\*Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="b11ff-110">Gli esempi dialin e MapName estendono la funzionalità NPS.</span><span class="sxs-lookup"><span data-stu-id="b11ff-110">The DialIn and MapName samples extend NPS functionality.</span></span>



| <span data-ttu-id="b11ff-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="b11ff-111">Sample</span></span>             | <span data-ttu-id="b11ff-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b11ff-112">Description</span></span>                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b11ff-113">DialIn</span><span class="sxs-lookup"><span data-stu-id="b11ff-113">DialIn</span></span><br/>  | <span data-ttu-id="b11ff-114">Questo esempio implementa una DLL di estensione RADIUS che controlla il bit di connessione per l'utente.</span><span class="sxs-lookup"><span data-stu-id="b11ff-114">This sample implements a RADIUS extension DLL that checks the dial-in bit for the user.</span></span><br/>                                                                                                              |
| <span data-ttu-id="b11ff-115">MapName</span><span class="sxs-lookup"><span data-stu-id="b11ff-115">MapName</span></span><br/> | <span data-ttu-id="b11ff-116">Questa DLL di estensione di esempio esegue la ricerca di tutti i domini trusted per l'account designato.</span><span class="sxs-lookup"><span data-stu-id="b11ff-116">This sample extension DLL searches all trusted domains for the designated account.</span></span> <span data-ttu-id="b11ff-117">Ciò consente di autenticare gli utenti di più domini senza che gli utenti debbano specificare il nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="b11ff-117">This allows users from multiple domains to be authenticated without the users having to supply their domain name.</span></span><br/> |



 

<span data-ttu-id="b11ff-118">È possibile trovare il codice sorgente per le applicazioni di esempio MapName e dialin nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="b11ff-118">You can find the source code for the MapName and DialIn sample applications in the following list.</span></span> <span data-ttu-id="b11ff-119">*Percorso*,% percorso di installazione%, designa la directory di installazione di base per i computer x64.</span><span class="sxs-lookup"><span data-stu-id="b11ff-119">*Location*, %Install Path%, designates the base installation directory for x64 computers.</span></span> <span data-ttu-id="b11ff-120">Vedere anche [Windows Software Development Kit (SDK) per Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK) e [download per lo sviluppo di applicazioni Windows Store](https://msdn.microsoft.com/windows/apps/br229516).</span><span class="sxs-lookup"><span data-stu-id="b11ff-120">See also [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK), and [Downloads for Windows Store app development](https://msdn.microsoft.com/windows/apps/br229516).</span></span>

<dl> <dt>

<span data-ttu-id="b11ff-121">Windows SDK per Windows 8</span><span class="sxs-lookup"><span data-stu-id="b11ff-121">Windows SDK for Windows 8</span></span>
</dt> <dd>

<span data-ttu-id="b11ff-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b11ff-122">Windows Server 2012</span></span>

<span data-ttu-id="b11ff-123">Collegamento di download: N/A</span><span class="sxs-lookup"><span data-stu-id="b11ff-123">Download link: N/A</span></span>

<span data-ttu-id="b11ff-124">MapName: No</span><span class="sxs-lookup"><span data-stu-id="b11ff-124">MapName: No</span></span>

<span data-ttu-id="b11ff-125">Dialin: No</span><span class="sxs-lookup"><span data-stu-id="b11ff-125">DialIn: No</span></span>

<span data-ttu-id="b11ff-126">Località: N/A</span><span class="sxs-lookup"><span data-stu-id="b11ff-126">Location: N/A</span></span>

</dd> <dt>

<span data-ttu-id="b11ff-127">Microsoft Windows Software Development Kit (SDK) per Windows 7 e .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="b11ff-127">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span>
</dt> <dd>

<span data-ttu-id="b11ff-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b11ff-128">Windows Server 2008 R2</span></span>

<span data-ttu-id="b11ff-129">Collegamento per il download: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span><span class="sxs-lookup"><span data-stu-id="b11ff-129">Download link: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279></span></span>

<span data-ttu-id="b11ff-130">MapName: Sì</span><span class="sxs-lookup"><span data-stu-id="b11ff-130">MapName: Yes</span></span>

<span data-ttu-id="b11ff-131">Dialin: No</span><span class="sxs-lookup"><span data-stu-id="b11ff-131">DialIn: No</span></span>

<span data-ttu-id="b11ff-132">Percorso:% install path% \\ Microsoft SDK \\ Windows \\ v 7.1 \\ Samples \\ netds \\ IAS</span><span class="sxs-lookup"><span data-stu-id="b11ff-132">Location: %Install Path%\\Microsoft SDKs\\Windows\\v7.1\\Samples\\netds\\ias</span></span>

</dd> <dt>

<span data-ttu-id="b11ff-133">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="b11ff-133">Windows SDK</span></span>
</dt> <dd>

<span data-ttu-id="b11ff-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b11ff-134">Windows Server 2008</span></span>

<span data-ttu-id="b11ff-135">Collegamento per il download: <https://www.microsoft.com/download/details.aspx?id=5023></span><span class="sxs-lookup"><span data-stu-id="b11ff-135">Download link: <https://www.microsoft.com/download/details.aspx?id=5023></span></span>

<span data-ttu-id="b11ff-136">MapName: Sì</span><span class="sxs-lookup"><span data-stu-id="b11ff-136">MapName: Yes</span></span>

<span data-ttu-id="b11ff-137">Dialin: No</span><span class="sxs-lookup"><span data-stu-id="b11ff-137">DialIn: No</span></span>

<span data-ttu-id="b11ff-138">Percorso:% install path% \\ Microsoft SDK \\ Windows \\ v 6.1 \\ Samples \\ NetDs \\ IAS</span><span class="sxs-lookup"><span data-stu-id="b11ff-138">Location: %Install Path%\\Microsoft SDKs\\Windows\\v6.1\\Samples\\NetDs\\IAS</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="b11ff-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b11ff-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b11ff-140">Download per sviluppatori</span><span class="sxs-lookup"><span data-stu-id="b11ff-140">Downloads for Developers</span></span>](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[<span data-ttu-id="b11ff-141">Windows SDK per Windows 8</span><span class="sxs-lookup"><span data-stu-id="b11ff-141">Windows SDK for Windows 8</span></span>](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





