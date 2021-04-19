---
description: La proprietà MSINEWINSTANCE indica l'installazione di una nuova istanza di un prodotto con le trasformazioni dell'istanza.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: Proprietà MSINEWINSTANCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8b51ec02d7b30c42e6e400b6a6177d7ef47d88c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330153"
---
# <a name="msinewinstance-property"></a><span data-ttu-id="04687-103">Proprietà MSINEWINSTANCE</span><span class="sxs-lookup"><span data-stu-id="04687-103">MSINEWINSTANCE property</span></span>

<span data-ttu-id="04687-104">La proprietà **MSINEWINSTANCE** indica l'installazione di una nuova istanza di un prodotto con le trasformazioni dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="04687-104">The **MSINEWINSTANCE** property indicates the installation of a new instance of a product with instance transforms.</span></span> <span data-ttu-id="04687-105">Questa proprietà supporta più istanze tramite codice del prodotto: modifica delle trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="04687-105">This property supports multiple instances through product code–changing transforms.</span></span> <span data-ttu-id="04687-106">Il valore di questa proprietà è 1.</span><span class="sxs-lookup"><span data-stu-id="04687-106">The value of this property is 1.</span></span> <span data-ttu-id="04687-107">Per la presenza di questa proprietà nella riga di comando è necessario che sia presente anche la proprietà [**TRANSformations**](transforms.md) .</span><span class="sxs-lookup"><span data-stu-id="04687-107">The presence of this property on the command line requires that the [**TRANSFORMS**](transforms.md) property also be present.</span></span> <span data-ttu-id="04687-108">La prima trasformazione elencata in **TRASformazioni** deve essere una trasformazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="04687-108">The first transform listed in **TRANSFORMS** must be an instance transform.</span></span> <span data-ttu-id="04687-109">Per ulteriori informazioni, vedere [installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md)</span><span class="sxs-lookup"><span data-stu-id="04687-109">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md)</span></span>

<span data-ttu-id="04687-110">Questa proprietà è disponibile con il programma di installazione che esegue un sistema in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="04687-110">This property is available with the installer running a system in the Windows Server 2003 or Windows XP.</span></span>

## <a name="requirements"></a><span data-ttu-id="04687-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04687-111">Requirements</span></span>



| <span data-ttu-id="04687-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="04687-112">Requirement</span></span> | <span data-ttu-id="04687-113">Valore</span><span class="sxs-lookup"><span data-stu-id="04687-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04687-114">Versione</span><span class="sxs-lookup"><span data-stu-id="04687-114">Version</span></span><br/> | <span data-ttu-id="04687-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="04687-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="04687-116">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="04687-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="04687-117">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="04687-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="04687-118">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="04687-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="04687-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04687-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04687-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="04687-120">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="04687-121">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="04687-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




