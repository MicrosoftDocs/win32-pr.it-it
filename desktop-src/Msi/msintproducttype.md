---
description: Il programma di installazione imposta la proprietà MsiNTProductType per i sistemi operativi Windows NT, Windows 2000 e versioni successive.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Proprietà MsiNTProductType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330149"
---
# <a name="msintproducttype-property"></a><span data-ttu-id="bdf3e-103">Proprietà MsiNTProductType</span><span class="sxs-lookup"><span data-stu-id="bdf3e-103">MsiNTProductType property</span></span>

<span data-ttu-id="bdf3e-104">Il programma di installazione imposta la proprietà **MsiNTProductType** per i sistemi operativi Windows NT, Windows 2000 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="bdf3e-104">The installer sets the **MsiNTProductType** property for Windows NT, Windows 2000, and later operating systems.</span></span> <span data-ttu-id="bdf3e-105">Questa proprietà indica il tipo di prodotto Windows.</span><span class="sxs-lookup"><span data-stu-id="bdf3e-105">This property indicates the Windows product type.</span></span>

<span data-ttu-id="bdf3e-106">Per i sistemi operativi Windows 2000 e versioni successive, il programma di installazione imposta i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bdf3e-106">For Windows 2000 and later operating systems, the installer sets the following values.</span></span> <span data-ttu-id="bdf3e-107">Si noti che i valori corrispondono a quelli del campo **wProductType** della struttura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="bdf3e-107">Note that values are the same as of the **wProductType** field of the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span>



| <span data-ttu-id="bdf3e-108">Valore</span><span class="sxs-lookup"><span data-stu-id="bdf3e-108">Value</span></span> | <span data-ttu-id="bdf3e-109">Significato</span><span class="sxs-lookup"><span data-stu-id="bdf3e-109">Meaning</span></span>                                  |
|-------|------------------------------------------|
| <span data-ttu-id="bdf3e-110">1</span><span class="sxs-lookup"><span data-stu-id="bdf3e-110">1</span></span>     | <span data-ttu-id="bdf3e-111">Windows 2000 Professional e versioni successive</span><span class="sxs-lookup"><span data-stu-id="bdf3e-111">Windows 2000 Professional and later</span></span>      |
| <span data-ttu-id="bdf3e-112">2</span><span class="sxs-lookup"><span data-stu-id="bdf3e-112">2</span></span>     | <span data-ttu-id="bdf3e-113">Controller di dominio Windows 2000 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="bdf3e-113">Windows 2000 domain controller and later</span></span> |
| <span data-ttu-id="bdf3e-114">3</span><span class="sxs-lookup"><span data-stu-id="bdf3e-114">3</span></span>     | <span data-ttu-id="bdf3e-115">Windows 2000 Server e versioni successive</span><span class="sxs-lookup"><span data-stu-id="bdf3e-115">Windows 2000 Server and later</span></span>            |



 

<span data-ttu-id="bdf3e-116">Per i sistemi operativi precedenti a Windows 2000, il programma di installazione imposta i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bdf3e-116">For operating systems earlier than Windows 2000, the installer sets the following values.</span></span>



| <span data-ttu-id="bdf3e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bdf3e-117">Value</span></span> | <span data-ttu-id="bdf3e-118">Significato</span><span class="sxs-lookup"><span data-stu-id="bdf3e-118">Meaning</span></span>                      |
|-------|------------------------------|
| <span data-ttu-id="bdf3e-119">1</span><span class="sxs-lookup"><span data-stu-id="bdf3e-119">1</span></span>     | <span data-ttu-id="bdf3e-120">Workstation Windows NT</span><span class="sxs-lookup"><span data-stu-id="bdf3e-120">Windows NT Workstation</span></span>       |
| <span data-ttu-id="bdf3e-121">2</span><span class="sxs-lookup"><span data-stu-id="bdf3e-121">2</span></span>     | <span data-ttu-id="bdf3e-122">Controller di dominio Windows NT</span><span class="sxs-lookup"><span data-stu-id="bdf3e-122">Windows NT domain controller</span></span> |
| <span data-ttu-id="bdf3e-123">3</span><span class="sxs-lookup"><span data-stu-id="bdf3e-123">3</span></span>     | <span data-ttu-id="bdf3e-124">Windows NT Server</span><span class="sxs-lookup"><span data-stu-id="bdf3e-124">Windows NT Server</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="bdf3e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdf3e-125">Requirements</span></span>



| <span data-ttu-id="bdf3e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdf3e-126">Requirement</span></span> | <span data-ttu-id="bdf3e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="bdf3e-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf3e-128">Versione</span><span class="sxs-lookup"><span data-stu-id="bdf3e-128">Version</span></span><br/> | <span data-ttu-id="bdf3e-129">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bdf3e-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bdf3e-130">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bdf3e-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bdf3e-131">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bdf3e-131">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bdf3e-132">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bdf3e-132">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bdf3e-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdf3e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdf3e-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bdf3e-134">Properties</span></span>](properties.md)
</dt> </dl>

 

 
