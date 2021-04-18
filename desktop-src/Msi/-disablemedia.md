---
description: L'impostazione della proprietà DISABLEMEDIA impedisce al programma di installazione di registrare qualsiasi origine multimediale, ad esempio un CD-ROM, come origine valida per il prodotto. Se l'esplorazione è abilitata, tuttavia, un utente può comunque passare a un'origine multimediale.
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: Proprietà DISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc1cad17269541fdb60573ae11065d485af9bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327818"
---
# <a name="disablemedia-property"></a><span data-ttu-id="decad-104">Proprietà DISABLEMEDIA</span><span class="sxs-lookup"><span data-stu-id="decad-104">DISABLEMEDIA property</span></span>

<span data-ttu-id="decad-105">L'impostazione della proprietà [**DISABLEMEDIA**](disablemedia.md) impedisce al programma di installazione di registrare qualsiasi origine multimediale, ad esempio un CD-ROM, come origine valida per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="decad-105">Setting the [**DISABLEMEDIA**](disablemedia.md) property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="decad-106">Se l'esplorazione è abilitata, tuttavia, un utente può comunque passare a un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="decad-106">If browsing is enabled, however, a user may still browse to a media source.</span></span>

## <a name="remarks"></a><span data-ttu-id="decad-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="decad-107">Remarks</span></span>

<span data-ttu-id="decad-108">Si noti che la proprietà [**DISABLEMEDIA**](disablemedia.md) ha un effetto diverso rispetto all'impostazione del criterio DISABLEMEDIA.</span><span class="sxs-lookup"><span data-stu-id="decad-108">Note that the [**DISABLEMEDIA**](disablemedia.md) property has a different effect than setting the DisableMedia policy.</span></span> <span data-ttu-id="decad-109">L'impostazione di **DISABLEMEDIA** impedisce la registrazione di qualsiasi origine multimediale, evitando al tempo stesso la prima installazione di un'applicazione da origini multimediali.</span><span class="sxs-lookup"><span data-stu-id="decad-109">Setting **DISABLEMEDIA** prevents the registration of any media source, and this also prevents the first time installation of an application from a media sources.</span></span>

<span data-ttu-id="decad-110">Per informazioni dettagliate sulla protezione delle origini multimediali di [*un'applicazione gestita*](m-gly.md) dall'esplorazione e dall'installazione da parte di utenti non amministratori, vedere [resilienza delle origini](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="decad-110">For details about securing the media sources of [*managed application*](m-gly.md) against browsing and installation by non-administrative users, see [Source Resiliency](source-resiliency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="decad-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="decad-111">Requirements</span></span>



| <span data-ttu-id="decad-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="decad-112">Requirement</span></span> | <span data-ttu-id="decad-113">Valore</span><span class="sxs-lookup"><span data-stu-id="decad-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="decad-114">Versione</span><span class="sxs-lookup"><span data-stu-id="decad-114">Version</span></span><br/> | <span data-ttu-id="decad-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="decad-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="decad-116">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="decad-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="decad-117">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="decad-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="decad-118">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="decad-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="decad-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="decad-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="decad-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="decad-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




