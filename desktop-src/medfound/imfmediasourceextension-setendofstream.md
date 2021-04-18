---
description: Indica che è stata raggiunta la fine del flusso multimediale.
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: 'Metodo IMFMediaSourceExtension:: SetEndOfStream'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetEndOfStream
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9018d76ce13bf441ea98134eb751f9e472f6bca8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320683"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a><span data-ttu-id="cbe88-103">Metodo IMFMediaSourceExtension:: SetEndOfStream</span><span class="sxs-lookup"><span data-stu-id="cbe88-103">IMFMediaSourceExtension::SetEndOfStream method</span></span>

<span data-ttu-id="cbe88-104">Indica che è stata raggiunta la fine del flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="cbe88-104">Indicate that the end of the media stream has been reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe88-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cbe88-105">Syntax</span></span>


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a><span data-ttu-id="cbe88-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cbe88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbe88-107">*errore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cbe88-107">*error* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe88-108">Utilizzato per passare le informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="cbe88-108">Used to pass error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbe88-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cbe88-109">Return value</span></span>

<span data-ttu-id="cbe88-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cbe88-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cbe88-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cbe88-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbe88-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbe88-112">Requirements</span></span>



| <span data-ttu-id="cbe88-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbe88-113">Requirement</span></span> | <span data-ttu-id="cbe88-114">Valore</span><span class="sxs-lookup"><span data-stu-id="cbe88-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe88-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbe88-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cbe88-116">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cbe88-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cbe88-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbe88-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cbe88-118">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cbe88-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cbe88-119">IDL</span><span class="sxs-lookup"><span data-stu-id="cbe88-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cbe88-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cbe88-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbe88-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbe88-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe88-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="cbe88-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> <dt>

[<span data-ttu-id="cbe88-123">**\_errore MF MSE \_**</span><span class="sxs-lookup"><span data-stu-id="cbe88-123">**MF\_MSE\_ERROR**</span></span>](mf-mse-error.md)
</dt> </dl>

 

 




