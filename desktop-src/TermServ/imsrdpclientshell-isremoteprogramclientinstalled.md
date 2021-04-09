---
title: Proprietà IsRemoteProgramClientInstalled di IMsRdpClientShell
description: Recupera un valore che indica se il client di Connessione Desktop remoto (RDC) supporta la funzionalità RemoteApp di Windows Server 2008 R2.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà IsRemoteProgramClientInstalled
- Servizi Desktop remoto proprietà IsRemoteProgramClientInstalled, interfaccia IMsRdpClientShell
- Interfaccia IMsRdpClientShell Servizi Desktop remoto, proprietà IsRemoteProgramClientInstalled
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787d45f10e109a89429be5032fda245aa3609567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119375"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a><span data-ttu-id="01a8f-106">Proprietà IMsRdpClientShell:: IsRemoteProgramClientInstalled</span><span class="sxs-lookup"><span data-stu-id="01a8f-106">IMsRdpClientShell::IsRemoteProgramClientInstalled property</span></span>

<span data-ttu-id="01a8f-107">Recupera un valore che indica se il client di Connessione Desktop remoto (RDC) supporta la funzionalità RemoteApp di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="01a8f-107">Retrieves whether the Remote Desktop Connection (RDC) client supports Windows Server 2008 R2 RemoteApp functionality.</span></span>

<span data-ttu-id="01a8f-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="01a8f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a8f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01a8f-109">Syntax</span></span>


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a><span data-ttu-id="01a8f-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="01a8f-110">Property value</span></span>

<span data-ttu-id="01a8f-111">Recupera un valore che indica se il client di Connessione Desktop remoto (RDC) supporta la funzionalità RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="01a8f-111">Retrieves whether the Remote Desktop Connection (RDC) client supports RemoteApp functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a8f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01a8f-112">Requirements</span></span>



| <span data-ttu-id="01a8f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="01a8f-113">Requirement</span></span> | <span data-ttu-id="01a8f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="01a8f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01a8f-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01a8f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="01a8f-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01a8f-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="01a8f-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01a8f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="01a8f-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01a8f-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="01a8f-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="01a8f-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="01a8f-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01a8f-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="01a8f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="01a8f-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01a8f-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01a8f-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="01a8f-123">IID</span><span class="sxs-lookup"><span data-stu-id="01a8f-123">IID</span></span><br/>                      | <span data-ttu-id="01a8f-124">IID \_ IMsRdpClientShell è definito come d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="01a8f-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="01a8f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01a8f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a8f-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="01a8f-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





