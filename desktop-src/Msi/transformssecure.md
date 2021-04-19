---
description: L'impostazione della proprietà TRANSFORMSSECURE su 1 informa il programma di installazione che le trasformazioni devono essere memorizzate nella cache localmente nel computer dell'utente in una posizione in cui l'utente non dispone dell'accesso in scrittura.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: Proprietà TRANSFORMSSECURE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b7a30ab5e94fb646e2e8960b60fd97dc35557c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333023"
---
# <a name="transformssecure-property"></a><span data-ttu-id="5acef-103">Proprietà TRANSFORMSSECURE</span><span class="sxs-lookup"><span data-stu-id="5acef-103">TRANSFORMSSECURE property</span></span>

<span data-ttu-id="5acef-104">L'impostazione della proprietà **TRANSFORMSSECURE** su 1 informa il programma di installazione che le trasformazioni devono essere memorizzate nella cache localmente nel computer dell'utente in una posizione in cui l'utente non dispone dell'accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="5acef-104">Setting the **TRANSFORMSSECURE** property to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="5acef-105">L'impostazione di questa proprietà è simile all'impostazione del [criterio TRANSFORMSSECURE](transformssecure-policy.md) , ad eccezione del fatto che l'ambito è diverso.</span><span class="sxs-lookup"><span data-stu-id="5acef-105">Setting this property is like setting the [TransformsSecure policy](transformssecure-policy.md) except that the scope is different.</span></span> <span data-ttu-id="5acef-106">L'impostazione del criterio TransformsSecure si applica a tutti i pacchetti installati da un determinato utente.</span><span class="sxs-lookup"><span data-stu-id="5acef-106">Setting TransformsSecure policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="5acef-107">L'impostazione della proprietà **TRANSFORMSSECURE** si applica al pacchetto indipendentemente dall'utente.</span><span class="sxs-lookup"><span data-stu-id="5acef-107">Setting the **TRANSFORMSSECURE** property applies to the package regardless of the user.</span></span>

<span data-ttu-id="5acef-108">Lo scopo di questa proprietà è fornire un'archiviazione sicura delle trasformazioni con gli utenti in viaggio di Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5acef-108">The purpose of this property is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="5acef-109">Quando questa proprietà è impostata, un' [installazione di manutenzione](maintenance-installation.md) può utilizzare solo la trasformazione dal percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="5acef-109">When this property is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the specified path.</span></span> <span data-ttu-id="5acef-110">Se il percorso non è disponibile, l'installazione di manutenzione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5acef-110">If the path is not available the maintenance installation fails.</span></span> <span data-ttu-id="5acef-111">Un'origine per ogni trasformazione protetta deve quindi risiedere nel percorso dell'origine del pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="5acef-111">A source for each secure transform must therefore reside at the location of the source of the installation package.</span></span> <span data-ttu-id="5acef-112">Se il programma di installazione rileva che la trasformazione non è presente nel computer locale, è possibile ripristinare la trasformazione da questa origine.</span><span class="sxs-lookup"><span data-stu-id="5acef-112">Then if the installer finds that the transform is missing on the local computer, it can restore the transform from this source.</span></span>

## <a name="remarks"></a><span data-ttu-id="5acef-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5acef-113">Remarks</span></span>

<span data-ttu-id="5acef-114">Windows Installer interpreta la proprietà [**TRANSFORMSATSOURCE**](transformsatsource.md) in modo che corrisponda alla proprietà **TRANSFORMSSECURE** .</span><span class="sxs-lookup"><span data-stu-id="5acef-114">Windows Installer interprets the [**TRANSFORMSATSOURCE**](transformsatsource.md) property to be the same as the **TRANSFORMSSECURE** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5acef-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5acef-115">Requirements</span></span>



| <span data-ttu-id="5acef-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5acef-116">Requirement</span></span> | <span data-ttu-id="5acef-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5acef-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5acef-118">Versione</span><span class="sxs-lookup"><span data-stu-id="5acef-118">Version</span></span><br/> | <span data-ttu-id="5acef-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5acef-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5acef-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5acef-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5acef-121">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5acef-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5acef-122">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5acef-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5acef-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5acef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5acef-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5acef-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="5acef-125">Trasformazioni di database</span><span class="sxs-lookup"><span data-stu-id="5acef-125">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




