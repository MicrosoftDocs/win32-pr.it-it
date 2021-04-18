---
description: La proprietà ComponentPath è una proprietà di sola lettura che restituisce il percorso completo di un componente installato. Se il percorso della chiave per il componente è una chiave del registro di sistema, viene restituita la chiave del registro di sistema.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Proprietà Installer. ComponentPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e249290af2477d2dfcbc73f80f80b439f1dd3663
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329027"
---
# <a name="installercomponentpath-property"></a><span data-ttu-id="e897e-104">Proprietà Installer. ComponentPath</span><span class="sxs-lookup"><span data-stu-id="e897e-104">Installer.ComponentPath property</span></span>

<span data-ttu-id="e897e-105">La proprietà **ComponentPath** è una proprietà di sola lettura che restituisce il percorso completo di un componente installato.</span><span class="sxs-lookup"><span data-stu-id="e897e-105">The **ComponentPath** property is a read-only property that returns the full path to an installed component.</span></span> <span data-ttu-id="e897e-106">Se il percorso della chiave per il componente è una chiave del registro di sistema, viene restituita la chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e897e-106">If the key path for the component is a registry key then the registry key is returned.</span></span>

<span data-ttu-id="e897e-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e897e-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e897e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e897e-108">Syntax</span></span>


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a><span data-ttu-id="e897e-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e897e-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="e897e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e897e-110">Remarks</span></span>

<span data-ttu-id="e897e-111">Se il componente è una chiave del registro di sistema, le radici del registro di sistema sono rappresentate numericamente.</span><span class="sxs-lookup"><span data-stu-id="e897e-111">If the component is a registry key, the registry roots are represented numerically.</span></span> <span data-ttu-id="e897e-112">Ad esempio, un percorso del registro di sistema "HKEY \_ Current \_ User \\ software \\ Microsoft" verrebbe restituito come "01: \\ software \\ Microsoft".</span><span class="sxs-lookup"><span data-stu-id="e897e-112">For example, a registry path of "HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft" would be returned as "01:\\SOFTWARE\\Microsoft".</span></span> <span data-ttu-id="e897e-113">Le radici del registro di sistema restituite sono definite come segue:</span><span class="sxs-lookup"><span data-stu-id="e897e-113">The registry roots returned are defined as follows:</span></span>



| <span data-ttu-id="e897e-114">Radice</span><span class="sxs-lookup"><span data-stu-id="e897e-114">Root</span></span>                    | <span data-ttu-id="e897e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e897e-115">Returned value</span></span> |
|-------------------------|----------------|
| <span data-ttu-id="e897e-116">HKEY\_CLASSI\_RADICE</span><span class="sxs-lookup"><span data-stu-id="e897e-116">HKEY\_CLASSES\_ROOT</span></span>     | <span data-ttu-id="e897e-117">00</span><span class="sxs-lookup"><span data-stu-id="e897e-117">00</span></span>             |
| <span data-ttu-id="e897e-118">HKEY\_CORRENTE\_UTENTE</span><span class="sxs-lookup"><span data-stu-id="e897e-118">HKEY\_CURRENT\_USER</span></span>     | <span data-ttu-id="e897e-119">01</span><span class="sxs-lookup"><span data-stu-id="e897e-119">01</span></span>             |
| <span data-ttu-id="e897e-120">HKEY\_LOCALE\_MACCHINA</span><span class="sxs-lookup"><span data-stu-id="e897e-120">HKEY\_LOCAL\_MACHINE</span></span>    | <span data-ttu-id="e897e-121">02</span><span class="sxs-lookup"><span data-stu-id="e897e-121">02</span></span>             |
| <span data-ttu-id="e897e-122">HKEY\_UTENTI</span><span class="sxs-lookup"><span data-stu-id="e897e-122">HKEY\_USERS</span></span>             | <span data-ttu-id="e897e-123">03</span><span class="sxs-lookup"><span data-stu-id="e897e-123">03</span></span>             |
| <span data-ttu-id="e897e-124">\_dati sulle prestazioni di HKEY \_</span><span class="sxs-lookup"><span data-stu-id="e897e-124">HKEY\_PERFORMANCE\_DATA</span></span> | <span data-ttu-id="e897e-125">04</span><span class="sxs-lookup"><span data-stu-id="e897e-125">04</span></span>             |



 

## <a name="requirements"></a><span data-ttu-id="e897e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e897e-126">Requirements</span></span>



| <span data-ttu-id="e897e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e897e-127">Requirement</span></span> | <span data-ttu-id="e897e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e897e-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e897e-129">Versione</span><span class="sxs-lookup"><span data-stu-id="e897e-129">Version</span></span><br/> | <span data-ttu-id="e897e-130">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e897e-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e897e-131">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e897e-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e897e-132">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="e897e-132">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e897e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e897e-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="e897e-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e897e-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e897e-135">IID</span><span class="sxs-lookup"><span data-stu-id="e897e-135">IID</span></span><br/>     | <span data-ttu-id="e897e-136">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e897e-136">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="e897e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e897e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e897e-138">**MsiGetComponentPath**</span><span class="sxs-lookup"><span data-stu-id="e897e-138">**MsiGetComponentPath**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




