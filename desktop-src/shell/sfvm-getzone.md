---
description: "Consente all'oggetto callback di fornire informazioni sull'area Internet. Usato da IShellFolderViewCB:: MessageSFVCB."
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: Messaggio SFVM_GETZONE (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5586188aeab6a054e22e4b242039beaae1ce390d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530181"
---
# <a name="sfvm_getzone-message"></a><span data-ttu-id="0ed88-104">SFVM \_ messaggio GETzone</span><span class="sxs-lookup"><span data-stu-id="0ed88-104">SFVM\_GETZONE message</span></span>

<span data-ttu-id="0ed88-105">\[Questa notifica è supportata tramite Windows XP Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0ed88-105">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="0ed88-106">Potrebbe non essere supportata nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0ed88-106">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0ed88-107">Consente all'oggetto callback di fornire informazioni sull'area Internet.</span><span class="sxs-lookup"><span data-stu-id="0ed88-107">Allows the callback object to provide Internet zone information.</span></span> <span data-ttu-id="0ed88-108">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="0ed88-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a><span data-ttu-id="0ed88-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ed88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ed88-110">*area* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="0ed88-110">*zone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed88-111">Uno dei valori seguenti che indica l'area Internet.</span><span class="sxs-lookup"><span data-stu-id="0ed88-111">One of the following values indicating the Internet zone.</span></span> <span data-ttu-id="0ed88-112">Questi valori costituiscono l'enumerazione [**urlzone**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) , definita in urlmon. h.</span><span class="sxs-lookup"><span data-stu-id="0ed88-112">These values constitute the [**URLZONE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) enumeration, defined in Urlmon.h.</span></span>

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span data-ttu-id="0ed88-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**\_computer locale \_ urlzone**</span><span class="sxs-lookup"><span data-stu-id="0ed88-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**URLZONE\_LOCAL\_MACHINE**</span></span>


</dt> <dd>

<span data-ttu-id="0ed88-114">Zona utilizzata per il contenuto già presente nel computer locale dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0ed88-114">Zone used for content already on the user's local computer.</span></span> <span data-ttu-id="0ed88-115">Questa zona non è esposta dall'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0ed88-115">This zone is not exposed by the user interface.</span></span>

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span data-ttu-id="0ed88-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**\_Intranet URLZONE**</span><span class="sxs-lookup"><span data-stu-id="0ed88-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**URLZONE\_INTRANET**</span></span>


</dt> <dd>

<span data-ttu-id="0ed88-117">Zona utilizzata per il contenuto presente in una rete Intranet.</span><span class="sxs-lookup"><span data-stu-id="0ed88-117">Zone used for content found on an intranet.</span></span>

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span data-ttu-id="0ed88-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE \_ attendibile**</span><span class="sxs-lookup"><span data-stu-id="0ed88-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE\_TRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="0ed88-119">Area usata per siti Web attendibili su Internet.</span><span class="sxs-lookup"><span data-stu-id="0ed88-119">Zone used for trusted websites on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span data-ttu-id="0ed88-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**\_Internet URLZONE**</span><span class="sxs-lookup"><span data-stu-id="0ed88-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**URLZONE\_INTERNET**</span></span>


</dt> <dd>

<span data-ttu-id="0ed88-121">Zona utilizzata per la maggior parte del contenuto su Internet.</span><span class="sxs-lookup"><span data-stu-id="0ed88-121">Zone used for most of the content on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span data-ttu-id="0ed88-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE non \_ attendibile**</span><span class="sxs-lookup"><span data-stu-id="0ed88-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE\_UNTRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="0ed88-123">Area usata per siti Web non attendibili.</span><span class="sxs-lookup"><span data-stu-id="0ed88-123">Zone used for websites that are not trusted.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ed88-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ed88-124">Requirements</span></span>



| <span data-ttu-id="0ed88-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ed88-125">Requirement</span></span> | <span data-ttu-id="0ed88-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0ed88-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed88-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ed88-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0ed88-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0ed88-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0ed88-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ed88-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0ed88-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0ed88-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0ed88-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ed88-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ed88-132"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ed88-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
