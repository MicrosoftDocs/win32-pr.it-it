---
title: Proprietà PCB IMsRdpClientSecuredSettings2
description: Specifica l'impostazione del BLOB di preconnessione (PCB) da usare prima della connessione per la trasmissione al server. | Proprietà PCB IMsRdpClientSecuredSettings2
ms.assetid: e2ddd9fd-d868-4fc5-835d-0f4db5da71e3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PCB
- Servizi Desktop remoto proprietà PCB, interfaccia IMsRdpClientSecuredSettings2
- Interfaccia IMsRdpClientSecuredSettings2 Servizi Desktop remoto, proprietà PCB
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2.PCB
- IMsRdpClientSecuredSettings2.get_PCB
- IMsRdpClientSecuredSettings2.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99b9a04a854f218fcbe1735ec6271aa4a58edba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321926"
---
# <a name="imsrdpclientsecuredsettings2pcb-property"></a><span data-ttu-id="fdcf3-107">IMsRdpClientSecuredSettings2::P la proprietà CB</span><span class="sxs-lookup"><span data-stu-id="fdcf3-107">IMsRdpClientSecuredSettings2::PCB property</span></span>

<span data-ttu-id="fdcf3-108">Specifica l'impostazione del BLOB di preconnessione (PCB) da usare prima della connessione per la trasmissione al server.</span><span class="sxs-lookup"><span data-stu-id="fdcf3-108">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="fdcf3-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fdcf3-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdcf3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fdcf3-110">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *bstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="fdcf3-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fdcf3-111">Property value</span></span>

<span data-ttu-id="fdcf3-112">Impostazione del PCB.</span><span class="sxs-lookup"><span data-stu-id="fdcf3-112">The PCB setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdcf3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdcf3-113">Requirements</span></span>



| <span data-ttu-id="fdcf3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdcf3-114">Requirement</span></span> | <span data-ttu-id="fdcf3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fdcf3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdcf3-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdcf3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fdcf3-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fdcf3-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="fdcf3-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdcf3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fdcf3-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdcf3-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fdcf3-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fdcf3-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="fdcf3-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdcf3-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fdcf3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fdcf3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdcf3-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdcf3-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdcf3-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdcf3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdcf3-125">**IMsRdpClientSecuredSettings2**</span><span class="sxs-lookup"><span data-stu-id="fdcf3-125">**IMsRdpClientSecuredSettings2**</span></span>](imsrdpclientsecuredsettings2.md)
</dt> </dl>

 

 





