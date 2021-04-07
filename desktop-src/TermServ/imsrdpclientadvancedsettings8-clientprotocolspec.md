---
title: Proprietà ClientProtocolSpec di IMsRdpClientAdvancedSettings8
description: Specifica il protocollo desktop remoto usato tra il client e il server.
ms.assetid: DD607D54-CAEA-43EE-94EB-F983AEA0CC1E
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ClientProtocolSpec
- Servizi Desktop remoto proprietà ClientProtocolSpec, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà ClientProtocolSpec
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings8.ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.get_ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.put_ClientProtocolSpec
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41e603f7587435b3701ec0511587286e1a38bcc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963905"
---
# <a name="imsrdpclientadvancedsettings8clientprotocolspec-property"></a><span data-ttu-id="47ba5-106">Proprietà IMsRdpClientAdvancedSettings8:: ClientProtocolSpec</span><span class="sxs-lookup"><span data-stu-id="47ba5-106">IMsRdpClientAdvancedSettings8::ClientProtocolSpec property</span></span>

<span data-ttu-id="47ba5-107">Specifica il protocollo desktop remoto usato tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="47ba5-107">Specifies the remote desktop protocol used between the client and the server.</span></span>

<span data-ttu-id="47ba5-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="47ba5-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="47ba5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47ba5-109">Syntax</span></span>


```C++
HRESULT put_ClientProtocolSpec(
  [in]  ClientSpec ClientMode
);

HRESULT get_ClientProtocolSpec(
  [out] ClientSpec *pClientMode
);
```



## <a name="property-value"></a><span data-ttu-id="47ba5-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="47ba5-110">Property value</span></span>

<span data-ttu-id="47ba5-111">Valore dell'enumerazione [**ClientSpec**](clientspec.md) che specifica il protocollo desktop remoto utilizzato tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="47ba5-111">A value of the [**ClientSpec**](clientspec.md) enumeration that specifies the remote desktop protocol used between the client and the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="47ba5-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47ba5-112">Requirements</span></span>



| <span data-ttu-id="47ba5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="47ba5-113">Requirement</span></span> | <span data-ttu-id="47ba5-114">Valore</span><span class="sxs-lookup"><span data-stu-id="47ba5-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47ba5-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47ba5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="47ba5-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="47ba5-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="47ba5-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47ba5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="47ba5-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="47ba5-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="47ba5-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="47ba5-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="47ba5-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47ba5-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="47ba5-121">DLL</span><span class="sxs-lookup"><span data-stu-id="47ba5-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47ba5-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47ba5-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47ba5-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47ba5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47ba5-124">**ClientSpec**</span><span class="sxs-lookup"><span data-stu-id="47ba5-124">**ClientSpec**</span></span>](clientspec.md)
</dt> <dt>

[<span data-ttu-id="47ba5-125">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="47ba5-125">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





