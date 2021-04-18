---
title: Proprietà TransportType di IMsRdpClientAdvancedSettings
description: Specifica il tipo di trasporto utilizzato dal client.
ms.assetid: 752f5fbc-eb5a-48eb-8750-fc25c8a2f024
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Proprietà TransportType
- Servizi Desktop remoto Proprietà TransportType, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, Proprietà TransportType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.TransportType
- IMsRdpClientAdvancedSettings.get_TransportType
- IMsRdpClientAdvancedSettings.put_TransportType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0664e0c792725dc112baf786d63c5175eb450dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300994"
---
# <a name="imsrdpclientadvancedsettingstransporttype-property"></a><span data-ttu-id="43ff0-106">Proprietà IMsRdpClientAdvancedSettings:: TransportType</span><span class="sxs-lookup"><span data-stu-id="43ff0-106">IMsRdpClientAdvancedSettings::TransportType property</span></span>

<span data-ttu-id="43ff0-107">Specifica il tipo di trasporto utilizzato dal client.</span><span class="sxs-lookup"><span data-stu-id="43ff0-107">Specifies the transport type used by the client.</span></span> <span data-ttu-id="43ff0-108">Questa proprietà non viene utilizzata dal controllo ActiveX Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="43ff0-108">This property is not used by the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="43ff0-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="43ff0-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ff0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43ff0-110">Syntax</span></span>


```C++
HRESULT put_TransportType(
  [in]  LONG transportType
);

HRESULT get_TransportType(
  [out] LONG *ptransportType
);
```



## <a name="property-value"></a><span data-ttu-id="43ff0-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="43ff0-111">Property value</span></span>

<span data-ttu-id="43ff0-112">Imposta il tipo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="43ff0-112">Sets the transport type.</span></span> <span data-ttu-id="43ff0-113">Questo metodo può avere esito positivo, ma il valore impostato non viene mai utilizzato dal controllo ActiveX Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="43ff0-113">This method may succeed, but the value set is never used by the Remote Desktop ActiveX control.</span></span>

## <a name="remarks"></a><span data-ttu-id="43ff0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="43ff0-114">Remarks</span></span>

<span data-ttu-id="43ff0-115">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="43ff0-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43ff0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43ff0-116">Requirements</span></span>



| <span data-ttu-id="43ff0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="43ff0-117">Requirement</span></span> | <span data-ttu-id="43ff0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="43ff0-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43ff0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43ff0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="43ff0-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43ff0-120">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="43ff0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43ff0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="43ff0-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43ff0-122">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="43ff0-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="43ff0-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="43ff0-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43ff0-124"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="43ff0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="43ff0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43ff0-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43ff0-126"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="43ff0-127">IID</span><span class="sxs-lookup"><span data-stu-id="43ff0-127">IID</span></span><br/>                      | <span data-ttu-id="43ff0-128">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="43ff0-128">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43ff0-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43ff0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43ff0-130">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="43ff0-130">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





