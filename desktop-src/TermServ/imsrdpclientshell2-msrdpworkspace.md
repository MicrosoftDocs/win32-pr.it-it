---
title: Proprietà MsRdpWorkspace di IMsRdpClientShell2
description: Recupera un puntatore all'interfaccia IMsRdpWorkspace, che consente di gestire le credenziali e le connessioni Connessione RemoteApp e desktop.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà MsRdpWorkspace
- Servizi Desktop remoto proprietà MsRdpWorkspace, interfaccia IMsRdpClientShell2
- Interfaccia IMsRdpClientShell2 Servizi Desktop remoto, proprietà MsRdpWorkspace
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91eadd3f1b422e3da96d5bcd3a5178a2a0b0eb52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742399"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a><span data-ttu-id="64cd2-106">Proprietà IMsRdpClientShell2:: MsRdpWorkspace</span><span class="sxs-lookup"><span data-stu-id="64cd2-106">IMsRdpClientShell2::MsRdpWorkspace property</span></span>

<span data-ttu-id="64cd2-107">Recupera un puntatore all'interfaccia [**IMsRdpWorkspace**](imsrdpworkspace.md) , che consente di gestire le credenziali e le connessioni connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="64cd2-107">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span>

<span data-ttu-id="64cd2-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="64cd2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="64cd2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64cd2-109">Syntax</span></span>


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a><span data-ttu-id="64cd2-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="64cd2-110">Property value</span></span>

<span data-ttu-id="64cd2-111">Indirizzo di un puntatore all'interfaccia [**IMsRdpWorkspace**](imsrdpworkspace.md) .</span><span class="sxs-lookup"><span data-stu-id="64cd2-111">The address of a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="64cd2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="64cd2-112">Remarks</span></span>

<span data-ttu-id="64cd2-113">L'interfaccia [**IMsRdpWorkspace**](imsrdpworkspace.md) non è esposta come interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="64cd2-113">The [**IMsRdpWorkspace**](imsrdpworkspace.md) interface is not exposed as a custom interface.</span></span> <span data-ttu-id="64cd2-114">È accessibile solo tramite metodi [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="64cd2-114">It is accessible through [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) methods only.</span></span>

## <a name="requirements"></a><span data-ttu-id="64cd2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64cd2-115">Requirements</span></span>



| <span data-ttu-id="64cd2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="64cd2-116">Requirement</span></span> | <span data-ttu-id="64cd2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="64cd2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="64cd2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64cd2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="64cd2-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="64cd2-119">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="64cd2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64cd2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="64cd2-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64cd2-121">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="64cd2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="64cd2-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64cd2-123"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64cd2-123"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64cd2-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64cd2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64cd2-125">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="64cd2-125">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

