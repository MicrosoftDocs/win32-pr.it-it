---
title: Proprietà UseRedirectionServerName di IMsRdpPreferredRedirectionInfo
description: Ottiene e imposta un valore che indica se utilizzare il nome del server di reindirizzamento.
ms.assetid: D2239600-D75D-40FB-A6D0-4C7C4C5163E3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà UseRedirectionServerName
- Servizi Desktop remoto proprietà UseRedirectionServerName, interfaccia IMsRdpPreferredRedirectionInfo
- Interfaccia IMsRdpPreferredRedirectionInfo Servizi Desktop remoto, proprietà UseRedirectionServerName
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo.UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.get_UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.put_UseRedirectionServerName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1635273078a2d09ca01c219ebf7eaa482eeb7a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740759"
---
# <a name="imsrdppreferredredirectioninfouseredirectionservername-property"></a><span data-ttu-id="62c48-106">Proprietà IMsRdpPreferredRedirectionInfo:: UseRedirectionServerName</span><span class="sxs-lookup"><span data-stu-id="62c48-106">IMsRdpPreferredRedirectionInfo::UseRedirectionServerName property</span></span>

<span data-ttu-id="62c48-107">Ottiene e imposta un valore che indica se utilizzare il nome del server di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="62c48-107">Gets and sets whether to use the redirection server name.</span></span>

<span data-ttu-id="62c48-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="62c48-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="62c48-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62c48-109">Syntax</span></span>


```C++
HRESULT put_UseRedirectionServerName(
  [in]  VARIANT_BOOL UseRedirectionServerName
);

HRESULT get_UseRedirectionServerName(
  [out] VARIANT_BOOL *UseRedirectionServerName
);
```



## <a name="property-value"></a><span data-ttu-id="62c48-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="62c48-110">Property value</span></span>

<span data-ttu-id="62c48-111">Indica se utilizzare il nome del server di reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="62c48-111">Whether to use the redirection server name.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c48-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62c48-112">Requirements</span></span>



| <span data-ttu-id="62c48-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c48-113">Requirement</span></span> | <span data-ttu-id="62c48-114">Valore</span><span class="sxs-lookup"><span data-stu-id="62c48-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62c48-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c48-115">Minimum supported client</span></span><br/> | <span data-ttu-id="62c48-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="62c48-116">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="62c48-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c48-117">Minimum supported server</span></span><br/> | <span data-ttu-id="62c48-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="62c48-118">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="62c48-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="62c48-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="62c48-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62c48-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="62c48-121">DLL</span><span class="sxs-lookup"><span data-stu-id="62c48-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62c48-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62c48-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="62c48-123">IID</span><span class="sxs-lookup"><span data-stu-id="62c48-123">IID</span></span><br/>                      | <span data-ttu-id="62c48-124">IID \_ IMsRdpPreferredRedirectionInfo è definito come FDD029F9-9574-4def-8529-64B521CCCAA4</span><span class="sxs-lookup"><span data-stu-id="62c48-124">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62c48-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62c48-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c48-126">**IMsRdpPreferredRedirectionInfo**</span><span class="sxs-lookup"><span data-stu-id="62c48-126">**IMsRdpPreferredRedirectionInfo**</span></span>](imsrdppreferredredirectioninfo.md)
</dt> </dl>

 

 





