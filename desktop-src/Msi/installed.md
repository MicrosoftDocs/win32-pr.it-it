---
description: La proprietà installata è impostata solo se il prodotto è installato per computer o per l'utente corrente.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Proprietà installata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330284"
---
# <a name="installed-property"></a><span data-ttu-id="a5649-103">Proprietà installata</span><span class="sxs-lookup"><span data-stu-id="a5649-103">Installed property</span></span>

<span data-ttu-id="a5649-104">La proprietà **installata** è impostata solo se il prodotto è installato per computer o per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="a5649-104">The **Installed** property is set only if the product is installed per-machine or for the current user.</span></span> <span data-ttu-id="a5649-105">Questa proprietà non viene impostata se il prodotto è installato per un utente diverso.</span><span class="sxs-lookup"><span data-stu-id="a5649-105">This property is not set if the product is installed for a different user.</span></span>

<span data-ttu-id="a5649-106">La proprietà **installata** può essere utilizzata nelle espressioni condizionali per determinare se un prodotto è installato per computer o per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="a5649-106">The **Installed** property can be used in conditional expressions to determine whether a product is installed per-computer or for the current user.</span></span> <span data-ttu-id="a5649-107">La proprietà, ad esempio, può essere utilizzata nella colonna condizionale di una tabella di sequenza o per distinguere tra una prima installazione e un'installazione di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="a5649-107">For example, the property can be used in the conditional column of a sequence table or to differentiate between a first installation and a maintenance installation.</span></span>

<span data-ttu-id="a5649-108">Per determinare se il prodotto è installato per un utente diverso, controllare la proprietà [**ProductState**](productstate.md) .</span><span class="sxs-lookup"><span data-stu-id="a5649-108">To determine whether the product is installed for a different user, check the [**ProductState**](productstate.md) property.</span></span>

<span data-ttu-id="a5649-109">Il valore della proprietà [**ProductVersion**](productversion.md) è la versione del prodotto in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="a5649-109">The value of the [**ProductVersion**](productversion.md) property is the version of the product in string format.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5649-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5649-110">Requirements</span></span>



| <span data-ttu-id="a5649-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5649-111">Requirement</span></span> | <span data-ttu-id="a5649-112">Valore</span><span class="sxs-lookup"><span data-stu-id="a5649-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5649-113">Versione</span><span class="sxs-lookup"><span data-stu-id="a5649-113">Version</span></span><br/> | <span data-ttu-id="a5649-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a5649-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a5649-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a5649-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a5649-116">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5649-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a5649-117">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a5649-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5649-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5649-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5649-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a5649-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




