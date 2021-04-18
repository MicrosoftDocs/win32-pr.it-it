---
description: Annulla l'operazione di trasferimento corrente.
ms.assetid: 42c6b2c3-7b6a-45d2-a7ce-844e95fe277b
title: 'Metodo IWiaTransfer:: Cancel (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Cancel
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 4764e922498a3c33278555cae37d09c1822959dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526460"
---
# <a name="iwiatransfercancel-method"></a><span data-ttu-id="06a9e-103">Metodo IWiaTransfer:: Cancel</span><span class="sxs-lookup"><span data-stu-id="06a9e-103">IWiaTransfer::Cancel method</span></span>

<span data-ttu-id="06a9e-104">Annulla l'operazione di trasferimento corrente.</span><span class="sxs-lookup"><span data-stu-id="06a9e-104">Cancels the current transfer operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a9e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06a9e-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="06a9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="06a9e-106">Parameters</span></span>

<span data-ttu-id="06a9e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="06a9e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="06a9e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06a9e-108">Return value</span></span>

<span data-ttu-id="06a9e-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="06a9e-109">Type: **HRESULT**</span></span>

<span data-ttu-id="06a9e-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="06a9e-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06a9e-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06a9e-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="06a9e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06a9e-112">Requirements</span></span>



| <span data-ttu-id="06a9e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="06a9e-113">Requirement</span></span> | <span data-ttu-id="06a9e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="06a9e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06a9e-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06a9e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="06a9e-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06a9e-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="06a9e-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06a9e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="06a9e-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06a9e-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="06a9e-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06a9e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="06a9e-120"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="06a9e-120"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="06a9e-121">IDL</span><span class="sxs-lookup"><span data-stu-id="06a9e-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06a9e-122"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="06a9e-122"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="06a9e-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="06a9e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="06a9e-124"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06a9e-124"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




