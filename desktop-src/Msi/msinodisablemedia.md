---
description: Impostare la proprietà MSINODISABLEMEDIA per impedire al programma di installazione di impostare la proprietà DISABLEMEDIA. L'impostazione della proprietà DISABLEMEDIA impedisce al programma di installazione di registrare qualsiasi origine multimediale, ad esempio un CD-ROM, come origine valida per il prodotto.
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: Proprietà MSINODISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93510263cbe182c66305dcc08c10d908709e1259
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330150"
---
# <a name="msinodisablemedia-property"></a><span data-ttu-id="f7876-104">Proprietà MSINODISABLEMEDIA</span><span class="sxs-lookup"><span data-stu-id="f7876-104">MSINODISABLEMEDIA property</span></span>

<span data-ttu-id="f7876-105">Impostare la proprietà **MSINODISABLEMEDIA** per impedire al programma di installazione di impostare la proprietà [**DISABLEMEDIA**](-disablemedia.md) .</span><span class="sxs-lookup"><span data-stu-id="f7876-105">Set the **MSINODISABLEMEDIA** property to prevent the installer from setting the [**DISABLEMEDIA**](-disablemedia.md) property.</span></span> <span data-ttu-id="f7876-106">L'impostazione della proprietà **DISABLEMEDIA** impedisce al programma di installazione di registrare qualsiasi origine multimediale, ad esempio un CD-ROM, come origine valida per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="f7876-106">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span>

<span data-ttu-id="f7876-107">Quando **MSINODISABLEMEDIA** non è impostato, il programma di installazione potrebbe aggiungere [**DISABLEMEDIA**](-disablemedia.md) al flusso di proprietà amministrative quando si esegue un' [installazione amministrativa](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="f7876-107">When **MSINODISABLEMEDIA** is not set, the installer might add [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream when performing an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="f7876-108">In questo modo si impedisce agli utenti che eseguono l'installazione dall'immagine amministrativa di eseguire l'installazione da un supporto, ad esempio un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="f7876-108">This prevents users who install from the administrative image from ever installing from media, such as a CD-ROM.</span></span>

-   <span data-ttu-id="f7876-109">Quando si esegue un'installazione amministrativa, il programma di installazione aggiunge [**DISABLEMEDIA**](-disablemedia.md) al flusso di proprietà amministrative solo se la proprietà di [**Riepilogo dei conteggi delle pagine**](page-count-summary.md) è inferiore a 150.</span><span class="sxs-lookup"><span data-stu-id="f7876-109">When performing an administrative installation, the installer only adds [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream if the [**Page Count Summary**](page-count-summary.md) Property is less than 150.</span></span>

<span data-ttu-id="f7876-110">Se [**DISABLEMEDIA**](-disablemedia.md) è elencato nella proprietà [**AdminProperties**](adminproperties.md) , l'impostazione **MSINODISABLEMEDIA** impedisce l'impostazione di **DISABLEMEDIA** durante un'installazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="f7876-110">If [**DISABLEMEDIA**](-disablemedia.md) is listed in the [**AdminProperties**](adminproperties.md) property, setting **MSINODISABLEMEDIA** prevents **DISABLEMEDIA** from being set during an administrative installation.</span></span> <span data-ttu-id="f7876-111">In questo caso, il programma di installazione può registrare un'origine multimediale e un utente può quindi avere la possibilità di reinstallare dall'origine multimediale se l'immagine di installazione amministrativa originale non è più disponibile in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="f7876-111">In this case, the installer may register a media source and a user could then have the option to reinstall from the media source if the original administrative installation image became unavailable later.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7876-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7876-112">Requirements</span></span>



| <span data-ttu-id="f7876-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7876-113">Requirement</span></span> | <span data-ttu-id="f7876-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f7876-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7876-115">Versione</span><span class="sxs-lookup"><span data-stu-id="f7876-115">Version</span></span><br/> | <span data-ttu-id="f7876-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f7876-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f7876-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f7876-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f7876-118">Windows Installer su Windows Server 2003, Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f7876-118">Windows Installer on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="f7876-119">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f7876-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7876-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7876-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7876-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7876-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




