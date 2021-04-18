---
title: Proprietà SecuredSettingsEnabled di IMsRdpClientShell2
description: Recupera un valore che indica se la pagina Web corrente si trova in un'area di protezione URL attendibile di Internet Explorer.
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClientShell2
- Interfaccia IMsRdpClientShell2 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1009759051207db7e6b8d741c1dd91e3de1ffc36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302462"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a><span data-ttu-id="783e0-106">Proprietà IMsRdpClientShell2:: SecuredSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="783e0-106">IMsRdpClientShell2::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="783e0-107">Recupera un valore che indica se la pagina Web corrente si trova in un'area di protezione URL attendibile di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="783e0-107">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

<span data-ttu-id="783e0-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="783e0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="783e0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="783e0-109">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="783e0-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="783e0-110">Property value</span></span>

<span data-ttu-id="783e0-111">Puntatore a un valore booleano che indica se la pagina Web corrente si trova in un'area di sicurezza URL di Internet Explorer attendibile.</span><span class="sxs-lookup"><span data-stu-id="783e0-111">A pointer to a Boolean value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="783e0-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="783e0-112">Requirements</span></span>



| <span data-ttu-id="783e0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="783e0-113">Requirement</span></span> | <span data-ttu-id="783e0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="783e0-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="783e0-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="783e0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="783e0-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="783e0-116">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="783e0-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="783e0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="783e0-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="783e0-118">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="783e0-119">DLL</span><span class="sxs-lookup"><span data-stu-id="783e0-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="783e0-120"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="783e0-120"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="783e0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="783e0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="783e0-122">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="783e0-122">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

 





