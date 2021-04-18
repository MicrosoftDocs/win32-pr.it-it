---
title: Proprietà ItsPubPlugin pluginName
description: Recupera il nome del plug-in.
ms.assetid: c1ea46b6-fac6-4140-a278-cb04ee9af739
ms.tgt_platform: multiple
keywords:
- Proprietà pluginName Servizi Desktop remoto
- Servizi Desktop remoto proprietà pluginName, interfaccia ItsPubPlugin
- Interfaccia ItsPubPlugin Servizi Desktop remoto, proprietà pluginName
topic_type:
- apiref
api_name:
- ItsPubPlugin.pluginName
- ItsPubPlugin.get_pluginName
api_location:
- Cpubplugin.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f5aa6ff6659047e9be48fd7b7a41f652c5cfd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301980"
---
# <a name="itspubpluginpluginname-property"></a><span data-ttu-id="71d5b-106">ItsPubPlugin::p proprietà luginName</span><span class="sxs-lookup"><span data-stu-id="71d5b-106">ItsPubPlugin::pluginName property</span></span>

<span data-ttu-id="71d5b-107">Recupera il nome del plug-in.</span><span class="sxs-lookup"><span data-stu-id="71d5b-107">Retrieves the name of the plug-in.</span></span>

<span data-ttu-id="71d5b-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="71d5b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d5b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71d5b-109">Syntax</span></span>


```C++
HRESULT get_pluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="71d5b-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="71d5b-110">Property value</span></span>

<span data-ttu-id="71d5b-111">Puntatore a una variabile **BSTR** per ricevere il nome del plug-in.</span><span class="sxs-lookup"><span data-stu-id="71d5b-111">A pointer to a **BSTR** variable to receive the name of the plug-in.</span></span>

## <a name="requirements"></a><span data-ttu-id="71d5b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71d5b-112">Requirements</span></span>



| <span data-ttu-id="71d5b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="71d5b-113">Requirement</span></span> | <span data-ttu-id="71d5b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="71d5b-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="71d5b-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71d5b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="71d5b-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="71d5b-116">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="71d5b-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71d5b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="71d5b-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="71d5b-118">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="71d5b-119">IDL</span><span class="sxs-lookup"><span data-stu-id="71d5b-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71d5b-120"><dt>Cpubplugin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71d5b-120"><dt>Cpubplugin.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71d5b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71d5b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d5b-122">**ItsPubPlugin**</span><span class="sxs-lookup"><span data-stu-id="71d5b-122">**ItsPubPlugin**</span></span>](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





