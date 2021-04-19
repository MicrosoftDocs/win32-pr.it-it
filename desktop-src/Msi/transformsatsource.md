---
description: L'impostazione di questa proprietà equivale a impostare i criteri del criterio TransformsAtSource, ad eccezione del fatto che l'ambito è diverso.
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: Proprietà TRANSFORMSATSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333022"
---
# <a name="transformsatsource-property"></a><span data-ttu-id="9f019-103">Proprietà TRANSFORMSATSOURCE</span><span class="sxs-lookup"><span data-stu-id="9f019-103">TRANSFORMSATSOURCE property</span></span>

<span data-ttu-id="9f019-104">L'impostazione di questa proprietà equivale a impostare i criteri del [criterio TransformsAtSource](transformsatsource-policy.md) , ad eccezione del fatto che l'ambito è diverso.</span><span class="sxs-lookup"><span data-stu-id="9f019-104">Setting this property is like setting the [TransformsAtSource policy](transformsatsource-policy.md) policy except that the scope is different.</span></span> <span data-ttu-id="9f019-105">L'impostazione del criterio TransformsAtSource si applica a tutti i pacchetti installati da un determinato utente.</span><span class="sxs-lookup"><span data-stu-id="9f019-105">Setting TransformsAtSource policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="9f019-106">L'impostazione della proprietà **TRANSFORMSATSOURCE** si applica al pacchetto indipendentemente dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="9f019-106">Setting the **TRANSFORMSATSOURCE** property applies to the package regardless of the users.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f019-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f019-107">Remarks</span></span>

<span data-ttu-id="9f019-108">Windows Installer interpreta la proprietà **TRANSFORMSATSOURCE** come se fosse la proprietà [**TRANSFORMSSECURE**](transformssecure.md) .</span><span class="sxs-lookup"><span data-stu-id="9f019-108">Windows Installer interprets the **TRANSFORMSATSOURCE** property as though it were the [**TRANSFORMSSECURE**](transformssecure.md) property.</span></span> <span data-ttu-id="9f019-109">Se il flag @ viene passato nella proprietà [**TRANSforms**](transforms.md) , Windows Installer considera le trasformazioni nell'elenco come [trasformazioni sicure all'origine](secure-at-source-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="9f019-109">If the @ flag is passed in the [**TRANSFORMS**](transforms.md) property, Windows Installer treats the transforms in the list as [secure-at-source transforms](secure-at-source-transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f019-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f019-110">Requirements</span></span>



| <span data-ttu-id="9f019-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f019-111">Requirement</span></span> | <span data-ttu-id="9f019-112">Valore</span><span class="sxs-lookup"><span data-stu-id="9f019-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f019-113">Versione</span><span class="sxs-lookup"><span data-stu-id="9f019-113">Version</span></span><br/> | <span data-ttu-id="9f019-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9f019-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9f019-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9f019-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9f019-116">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9f019-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9f019-117">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9f019-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9f019-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f019-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f019-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f019-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




