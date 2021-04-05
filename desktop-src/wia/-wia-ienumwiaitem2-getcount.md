---
description: Restituisce il numero di elementi archiviati da questo enumeratore.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: 'Metodo IEnumWiaItem2:: GetCount (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 23c067b8e4da93d678f641890a85e2535b3ca50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049595"
---
# <a name="ienumwiaitem2getcount-method"></a><span data-ttu-id="af787-103">Metodo IEnumWiaItem2:: GetCount</span><span class="sxs-lookup"><span data-stu-id="af787-103">IEnumWiaItem2::GetCount method</span></span>

<span data-ttu-id="af787-104">Restituisce il numero di elementi archiviati da questo enumeratore.</span><span class="sxs-lookup"><span data-stu-id="af787-104">Returns the number of elements stored by this enumerator.</span></span>

## <a name="syntax"></a><span data-ttu-id="af787-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af787-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a><span data-ttu-id="af787-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="af787-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af787-107">*cElt* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="af787-107">*cElt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af787-108">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="af787-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="af787-109">Riceve un puntatore a un _ *ULONG*\* che riceve il numero di elementi nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="af787-109">Receives a pointer to a _ *ULONG*\* that receives the number of elements in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af787-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af787-110">Return value</span></span>

<span data-ttu-id="af787-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="af787-111">Type: **HRESULT**</span></span>

<span data-ttu-id="af787-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="af787-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="af787-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="af787-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="af787-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af787-114">Requirements</span></span>



| <span data-ttu-id="af787-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="af787-115">Requirement</span></span> | <span data-ttu-id="af787-116">Valore</span><span class="sxs-lookup"><span data-stu-id="af787-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af787-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af787-117">Minimum supported client</span></span><br/> | <span data-ttu-id="af787-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af787-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="af787-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af787-119">Minimum supported server</span></span><br/> | <span data-ttu-id="af787-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="af787-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="af787-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af787-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="af787-122"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="af787-122"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="af787-123">IDL</span><span class="sxs-lookup"><span data-stu-id="af787-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="af787-124"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="af787-124"><dt>Wia.idl</dt></span></span> </dl> |



 

 




