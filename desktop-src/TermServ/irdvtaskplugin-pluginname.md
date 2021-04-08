---
title: Proprietà IRDVTaskPlugin pluginName (Tspubplugincom. h)
description: Contiene il nome visualizzato dell'agente attività.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- Proprietà pluginName Servizi Desktop remoto
- Servizi Desktop remoto proprietà pluginName, interfaccia IRDVTaskPlugin
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto, proprietà pluginName
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0262472e37a8ff3e5b9bb153d2e94f4e52029b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742074"
---
# <a name="irdvtaskpluginpluginname-property"></a><span data-ttu-id="810be-106">IRDVTaskPlugin::P proprietà luginName</span><span class="sxs-lookup"><span data-stu-id="810be-106">IRDVTaskPlugin::PluginName property</span></span>

<span data-ttu-id="810be-107">Contiene il nome visualizzato dell'agente attività.</span><span class="sxs-lookup"><span data-stu-id="810be-107">Contains the display name of the task agent.</span></span> <span data-ttu-id="810be-108">Questo nome viene utilizzato solo a scopo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="810be-108">This name is used for logging purposes only.</span></span>

<span data-ttu-id="810be-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="810be-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="810be-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="810be-110">Syntax</span></span>


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="810be-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="810be-111">Property value</span></span>

<span data-ttu-id="810be-112">Nome visualizzato dell'agente attività.</span><span class="sxs-lookup"><span data-stu-id="810be-112">The display name of the task agent.</span></span>

## <a name="requirements"></a><span data-ttu-id="810be-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="810be-113">Requirements</span></span>



| <span data-ttu-id="810be-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="810be-114">Requirement</span></span> | <span data-ttu-id="810be-115">Valore</span><span class="sxs-lookup"><span data-stu-id="810be-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="810be-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="810be-116">Minimum supported client</span></span><br/> | <span data-ttu-id="810be-117">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="810be-117">Windows 7 Enterprise</span></span><br/>                                                             |
| <span data-ttu-id="810be-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="810be-118">Minimum supported server</span></span><br/> | <span data-ttu-id="810be-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="810be-119">Windows Server 2008 R2</span></span><br/>                                                           |
| <span data-ttu-id="810be-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="810be-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="810be-121"><dt>Tspubplugincom. h</dt></span><span class="sxs-lookup"><span data-stu-id="810be-121"><dt>Tspubplugincom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="810be-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="810be-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="810be-123">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="810be-123">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





