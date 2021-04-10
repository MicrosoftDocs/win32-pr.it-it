---
description: Ignora il numero specificato di elementi durante un'enumerazione degli oggetti IWiaItem2 disponibili.
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: 'Metodo IEnumWiaItem2:: Skip (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7618aad923136a9a32d8b7fb935050fefe07bff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966844"
---
# <a name="ienumwiaitem2skip-method"></a><span data-ttu-id="3b7a8-103">Metodo IEnumWiaItem2:: Skip</span><span class="sxs-lookup"><span data-stu-id="3b7a8-103">IEnumWiaItem2::Skip method</span></span>

<span data-ttu-id="3b7a8-104">Ignora il numero specificato di elementi durante un'enumerazione degli oggetti [**IWiaItem2**](-wia-iwiaitem2.md) disponibili.</span><span class="sxs-lookup"><span data-stu-id="3b7a8-104">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b7a8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b7a8-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a><span data-ttu-id="3b7a8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b7a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b7a8-107">*cElt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b7a8-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7a8-108">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="3b7a8-108">Type: **ULONG**</span></span>

<span data-ttu-id="3b7a8-109">Specifica il numero di elementi da ignorare.</span><span class="sxs-lookup"><span data-stu-id="3b7a8-109">Specifies the number of items to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b7a8-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b7a8-110">Return value</span></span>

<span data-ttu-id="3b7a8-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3b7a8-111">Type: **HRESULT**</span></span>

<span data-ttu-id="3b7a8-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3b7a8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3b7a8-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b7a8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b7a8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b7a8-114">Requirements</span></span>



| <span data-ttu-id="3b7a8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b7a8-115">Requirement</span></span> | <span data-ttu-id="3b7a8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3b7a8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3b7a8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b7a8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3b7a8-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b7a8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3b7a8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b7a8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3b7a8-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3b7a8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3b7a8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b7a8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b7a8-122"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b7a8-122"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b7a8-123">IDL</span><span class="sxs-lookup"><span data-stu-id="3b7a8-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b7a8-124"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b7a8-124"><dt>Wia.idl</dt></span></span> </dl> |



 

 




