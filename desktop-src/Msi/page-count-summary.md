---
description: La proprietà riepilogo conteggio pagine contiene la versione minima del programma di installazione richiesta dal pacchetto di installazione.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Proprietà riepilogo conteggio pagine
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec5e319450bb7a7db5515587be7777ad3e657d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329746"
---
# <a name="page-count-summary-property"></a><span data-ttu-id="bcc75-103">Proprietà riepilogo conteggio pagine</span><span class="sxs-lookup"><span data-stu-id="bcc75-103">Page Count Summary property</span></span>

<span data-ttu-id="bcc75-104">La proprietà **Riepilogo conteggio pagine** contiene la versione minima del programma di installazione richiesta dal pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="bcc75-104">The **Page Count Summary** property contains the minimum installer version required by the installation package.</span></span> <span data-ttu-id="bcc75-105">Per un minimo di Windows Installer 2,0, questa proprietà deve essere impostata sul valore integer 200.</span><span class="sxs-lookup"><span data-stu-id="bcc75-105">For a minimum of Windows Installer 2.0, this property must be set to the integer 200.</span></span> <span data-ttu-id="bcc75-106">Per un minimo di Windows Installer 3,0, questa proprietà deve essere impostata sul valore integer 300.</span><span class="sxs-lookup"><span data-stu-id="bcc75-106">For a minimum of Windows Installer 3.0, this property must be set to the integer 300.</span></span> <span data-ttu-id="bcc75-107">Per un minimo di Windows Installer 3,1, questa proprietà deve essere impostata su 301.</span><span class="sxs-lookup"><span data-stu-id="bcc75-107">For a minimum of Windows Installer 3.1, this property must be set to 301.</span></span> <span data-ttu-id="bcc75-108">Per un minimo di Windows Installer 4,5, questa proprietà deve essere impostata su 405.</span><span class="sxs-lookup"><span data-stu-id="bcc75-108">For a minimum of Windows Installer 4.5, this property must be set to 405.</span></span> <span data-ttu-id="bcc75-109">Per un minimo di Windows Installer 5,0, questa proprietà deve essere impostata su 500.</span><span class="sxs-lookup"><span data-stu-id="bcc75-109">For a minimum of Windows Installer 5.0, this property must be set to 500.</span></span>

<span data-ttu-id="bcc75-110">Per i [pacchetti di Windows Installer a 64 bit](64-bit-windows-installer-packages.md), questa proprietà deve essere impostata sul valore integer 200 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="bcc75-110">For [64-bit Windows Installer Packages](64-bit-windows-installer-packages.md), this property must be set to the integer 200 or greater.</span></span> <span data-ttu-id="bcc75-111">Per i pacchetti di Windows Installer a 64 bit nella piattaforma Arm64, questa proprietà deve essere impostata sul valore integer 500 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="bcc75-111">For 64-bit Windows Installer Packages on the Arm64 platform, this property must be set to the integer 500 or greater.</span></span>

<span data-ttu-id="bcc75-112">Per un pacchetto di trasformazione, la proprietà **Riepilogo conteggio pagine** contiene la versione minima del programma di installazione necessaria per elaborare la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="bcc75-112">For a transform package, the **Page Count Summary** property contains the minimum installer version required to process the transform.</span></span> <span data-ttu-id="bcc75-113">Impostare su un valore maggiore dei due valori delle proprietà di **Riepilogo dei conteggi delle pagine** che appartengono ai database utilizzati per generare la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="bcc75-113">Set to the greater of the two **Page Count Summary** property values that belong to the databases used to generate the transform.</span></span>

<span data-ttu-id="bcc75-114">Per un pacchetto di patch, la proprietà di **Riepilogo di conteggio pagine** è impostata su null.</span><span class="sxs-lookup"><span data-stu-id="bcc75-114">For a patch package, the **Page Count Summary** property is set to Null.</span></span>

<span data-ttu-id="bcc75-115">Questa proprietà di riepilogo è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="bcc75-115">This summary property is required.</span></span>

<span data-ttu-id="bcc75-116">Questa proprietà può essere utilizzata per creare un pacchetto che può essere installato solo dalla versione minima o successiva specificata della Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bcc75-116">This property can be used to author a package that can be installed only by the specified minimum or later version of the Windows Installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcc75-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcc75-117">Requirements</span></span>



| <span data-ttu-id="bcc75-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcc75-118">Requirement</span></span> | <span data-ttu-id="bcc75-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bcc75-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcc75-120">Versione</span><span class="sxs-lookup"><span data-stu-id="bcc75-120">Version</span></span><br/> | <span data-ttu-id="bcc75-121">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bcc75-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bcc75-122">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bcc75-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bcc75-123">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="bcc75-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bcc75-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcc75-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcc75-125">Descrizioni delle proprietà di riepilogo</span><span class="sxs-lookup"><span data-stu-id="bcc75-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




