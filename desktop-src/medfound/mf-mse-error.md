---
description: Definisce i diversi Stati di errore dell'estensione di origine multimediale.
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: Enumerazione MF_MSE_ERROR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 6b6aaea772376b0e57c006a56a5a1bb30bc497c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130718"
---
# <a name="mf_mse_error-enumeration"></a><span data-ttu-id="d486d-103">\_ \_ Enumerazione errori MF MSE</span><span class="sxs-lookup"><span data-stu-id="d486d-103">MF\_MSE\_ERROR enumeration</span></span>

<span data-ttu-id="d486d-104">Definisce i diversi Stati di errore dell'estensione di origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="d486d-104">Defines the different error states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="d486d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d486d-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a><span data-ttu-id="d486d-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="d486d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d486d-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**\_errore MF \_ MSE \_ NOERROR**</span><span class="sxs-lookup"><span data-stu-id="d486d-107"><span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF\_MSE\_ERROR\_NOERROR**</span></span>
</dt> <dd>

<span data-ttu-id="d486d-108">Non specifica alcun errore.</span><span class="sxs-lookup"><span data-stu-id="d486d-108">Specifies no error.</span></span>

</dd> <dt>

<span data-ttu-id="d486d-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**\_rete di \_ errori MF MSE \_**</span><span class="sxs-lookup"><span data-stu-id="d486d-109"><span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**MF\_MSE\_ERROR\_NETWORK**</span></span>
</dt> <dd>

<span data-ttu-id="d486d-110">Specifica un errore con la rete.</span><span class="sxs-lookup"><span data-stu-id="d486d-110">Specifies an error with the network.</span></span>

</dd> <dt>

<span data-ttu-id="d486d-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**\_ \_ decodifica errore MF \_ MSE**</span><span class="sxs-lookup"><span data-stu-id="d486d-111"><span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**MF\_MSE\_ERROR\_DECODE**</span></span>
</dt> <dd>

<span data-ttu-id="d486d-112">Specifica un errore di decodifica.</span><span class="sxs-lookup"><span data-stu-id="d486d-112">Specifies an error with decoding.</span></span>

</dd> <dt>

<span data-ttu-id="d486d-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**errore di MF \_ MSE \_ \_ sconosciuto \_**</span><span class="sxs-lookup"><span data-stu-id="d486d-113"><span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**MF\_MSE\_ERROR\_UNKNOWN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="d486d-114">Specifica un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="d486d-114">Specifies an unknown error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d486d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d486d-115">Requirements</span></span>



| <span data-ttu-id="d486d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d486d-116">Requirement</span></span> | <span data-ttu-id="d486d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d486d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d486d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d486d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d486d-119">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d486d-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d486d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d486d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d486d-121">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d486d-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d486d-122">IDL</span><span class="sxs-lookup"><span data-stu-id="d486d-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d486d-123"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d486d-123"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d486d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d486d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d486d-125">Enumerazioni di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d486d-125">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




