---
title: Proprietà RemoteMonitorLayoutMatchesLocal di IMsRdpClientNonScriptable5
description: Specifica se il layout di monitoraggio remoto è identico a quello del monitoraggio locale.
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RemoteMonitorLayoutMatchesLocal
- Servizi Desktop remoto proprietà RemoteMonitorLayoutMatchesLocal, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà RemoteMonitorLayoutMatchesLocal
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5018b22865cc683fc9231c857a1b99b8acbfeca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120398"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a><span data-ttu-id="cef6d-106">Proprietà IMsRdpClientNonScriptable5:: RemoteMonitorLayoutMatchesLocal</span><span class="sxs-lookup"><span data-stu-id="cef6d-106">IMsRdpClientNonScriptable5::RemoteMonitorLayoutMatchesLocal property</span></span>

<span data-ttu-id="cef6d-107">Specifica se il layout di monitoraggio remoto è identico a quello del monitoraggio locale.</span><span class="sxs-lookup"><span data-stu-id="cef6d-107">Specifies if the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="cef6d-108">Se questa proprietà contiene la **variante \_ true**, il layout del monitor remoto è identico al layout di monitoraggio locale.</span><span class="sxs-lookup"><span data-stu-id="cef6d-108">If this property contains **VARIANT\_TRUE**, the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="cef6d-109">Se questa proprietà contiene la **variante \_ false**, i monitoraggi locali e remoti hanno layout diversi.</span><span class="sxs-lookup"><span data-stu-id="cef6d-109">If this property contains **VARIANT\_FALSE**, the remote and local monitors have different layouts.</span></span>

<span data-ttu-id="cef6d-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cef6d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cef6d-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cef6d-111">Syntax</span></span>


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a><span data-ttu-id="cef6d-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="cef6d-112">Property value</span></span>

<span data-ttu-id="cef6d-113">Riceve il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="cef6d-113">Receives the property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cef6d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cef6d-114">Requirements</span></span>



| <span data-ttu-id="cef6d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cef6d-115">Requirement</span></span> | <span data-ttu-id="cef6d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cef6d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cef6d-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cef6d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cef6d-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cef6d-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cef6d-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cef6d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cef6d-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cef6d-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="cef6d-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="cef6d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="cef6d-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cef6d-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="cef6d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cef6d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cef6d-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cef6d-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="cef6d-125">IID</span><span class="sxs-lookup"><span data-stu-id="cef6d-125">IID</span></span><br/>                      | <span data-ttu-id="cef6d-126">IID \_ IMsRdpClientNonScriptable5 è definito come 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="cef6d-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cef6d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cef6d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cef6d-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="cef6d-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





