---
description: Generato dal motore dei criteri quando l'individualizzazione sta per iniziare. L'individualizzazione viene eseguita usando l'implementazione delle applicazioni dell'interfaccia IMFContentProtectionManager.
ms.assetid: a3ba98ee-4d2e-466d-be9a-c7e3b5f920a7
title: Evento MEIndividualizationStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb8d50bbc2081c4efa41d8b15cc3e41a14ab5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309637"
---
# <a name="meindividualizationstart-event"></a><span data-ttu-id="69996-104">Evento MEIndividualizationStart</span><span class="sxs-lookup"><span data-stu-id="69996-104">MEIndividualizationStart event</span></span>

<span data-ttu-id="69996-105">Generato dal motore dei criteri quando l'individualizzazione sta per iniziare.</span><span class="sxs-lookup"><span data-stu-id="69996-105">Raised by the policy engine when individualization is about to begin.</span></span> <span data-ttu-id="69996-106">L'individualizzazione viene eseguita usando l'implementazione dell'applicazione dell'interfaccia [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) .</span><span class="sxs-lookup"><span data-stu-id="69996-106">Individualization is performed using the application's implementation of the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

<span data-ttu-id="69996-107">Un'applicazione personalizzata è una che ha ricevuto un aggiornamento ai componenti di Digital Rights Management (DRM) che li distingue da tutte le altre copie della stessa applicazione.</span><span class="sxs-lookup"><span data-stu-id="69996-107">An individualized application is one that has received an upgrade to its digital rights management (DRM) components that differentiates it from all other copies of the same application.</span></span> <span data-ttu-id="69996-108">I proprietari del contenuto possono richiedere che i file protetti vengano riprodotti solo in un'applicazione che è stata individualmente.</span><span class="sxs-lookup"><span data-stu-id="69996-108">Content owners can require that their protected files be played only on an application that has been individualized.</span></span>

## <a name="event-values"></a><span data-ttu-id="69996-109">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="69996-109">Event values</span></span>

<span data-ttu-id="69996-110">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="69996-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="69996-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="69996-111">VARTYPE</span></span>              | <span data-ttu-id="69996-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69996-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="69996-113">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="69996-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="69996-114">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="69996-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="69996-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="69996-115">Remarks</span></span>

<span data-ttu-id="69996-116">Quando l'acquisizione della licenza viene completata, il motore dei criteri genera l'evento [MEIndividualizationCompleted](meindividualizationcompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="69996-116">When license acquisition is completed, the policy engine raises the [MEIndividualizationCompleted](meindividualizationcompleted.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="69996-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69996-117">Requirements</span></span>



| <span data-ttu-id="69996-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="69996-118">Requirement</span></span> | <span data-ttu-id="69996-119">Valore</span><span class="sxs-lookup"><span data-stu-id="69996-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69996-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69996-120">Minimum supported client</span></span><br/> | <span data-ttu-id="69996-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69996-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="69996-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69996-122">Minimum supported server</span></span><br/> | <span data-ttu-id="69996-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="69996-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="69996-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69996-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="69996-125"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69996-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69996-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69996-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69996-127">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69996-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




