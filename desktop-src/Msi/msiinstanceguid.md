---
description: La presenza della proprietà MSIINSTANCEGUID indica che un codice prodotto&\# 8211; la modifica della trasformazione è registrata nel prodotto.
ms.assetid: c39be15d-e10a-4055-bd81-aa7510a19fe4
title: Proprietà MSIINSTANCEGUID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c798d56cf3ede6a75a133dd7e0ec7f42c32e84f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325462"
---
# <a name="msiinstanceguid-property"></a><span data-ttu-id="70838-103">Proprietà MSIINSTANCEGUID</span><span class="sxs-lookup"><span data-stu-id="70838-103">MSIINSTANCEGUID property</span></span>

<span data-ttu-id="70838-104">La presenza della proprietà **MSIINSTANCEGUID** indica che nel prodotto è registrata una trasformazione che modifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="70838-104">The presence of the **MSIINSTANCEGUID** property indicates that a product code–changing transform is registered to the product.</span></span> <span data-ttu-id="70838-105">Il valore della proprietà **MSIINSTANCEGUID** specifica quale istanza di un prodotto deve essere utilizzata per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="70838-105">The value of the **MSIINSTANCEGUID** property specifies which instance of a product is to be used for installation.</span></span> <span data-ttu-id="70838-106">La proprietà **MSIINSTANCEGUID** può fare riferimento solo a un prodotto che è già stato installato con una trasformazione istanza.</span><span class="sxs-lookup"><span data-stu-id="70838-106">The **MSIINSTANCEGUID** property can only reference a product that has already been installed with an instance transform.</span></span>

<span data-ttu-id="70838-107">Le trasformazioni dell'istanza sono codice del prodotto: modifica delle trasformazioni disponibili con il programma di installazione in esecuzione in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70838-107">Instance transforms are product code–changing transforms available with the installer running on either Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="70838-108">Per ulteriori informazioni, vedere [installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="70838-108">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70838-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70838-109">Requirements</span></span>



| <span data-ttu-id="70838-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="70838-110">Requirement</span></span> | <span data-ttu-id="70838-111">Valore</span><span class="sxs-lookup"><span data-stu-id="70838-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70838-112">Versione</span><span class="sxs-lookup"><span data-stu-id="70838-112">Version</span></span><br/> | <span data-ttu-id="70838-113">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="70838-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="70838-114">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="70838-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="70838-115">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70838-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="70838-116">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="70838-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70838-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70838-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70838-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="70838-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="70838-119">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="70838-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




