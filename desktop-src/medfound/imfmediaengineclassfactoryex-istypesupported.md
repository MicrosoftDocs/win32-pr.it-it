---
description: Ottiene un valore che indica se il sistema di chiavi specificato supporta il tipo di supporto specificato.
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: 'Metodo IMFMediaEngineClassFactoryEx:: IsTypeSupported'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320473"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a><span data-ttu-id="673e4-103">Metodo IMFMediaEngineClassFactoryEx:: IsTypeSupported</span><span class="sxs-lookup"><span data-stu-id="673e4-103">IMFMediaEngineClassFactoryEx::IsTypeSupported method</span></span>

<span data-ttu-id="673e4-104">Ottiene un valore che indica se il sistema di chiavi specificato supporta il tipo di supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="673e4-104">Gets a value that indicates if the specified key system supports the specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="673e4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="673e4-105">Syntax</span></span>


```C++
HRESULT IsTypeSupported(
   BSTR type,
   BSTR keySystem,
   BOOL *isSupported
);
```



## <a name="parameters"></a><span data-ttu-id="673e4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="673e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="673e4-107">*type*</span><span class="sxs-lookup"><span data-stu-id="673e4-107">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="673e4-108">Tipo MIME per cui verificare il supporto.</span><span class="sxs-lookup"><span data-stu-id="673e4-108">The MIME type to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="673e4-109">*Sistema*</span><span class="sxs-lookup"><span data-stu-id="673e4-109">*keySystem*</span></span> 
</dt> <dd>

<span data-ttu-id="673e4-110">Sistema di chiavi di cui verificare il supporto.</span><span class="sxs-lookup"><span data-stu-id="673e4-110">The key system to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="673e4-111">*isSupported*</span><span class="sxs-lookup"><span data-stu-id="673e4-111">*isSupported*</span></span> 
</dt> <dd>

<span data-ttu-id="673e4-112">**true** se il tipo è supportato da un *sistema*. in caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="673e4-112">**true** if type is supported by *keySystem*; otherwise, **false.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="673e4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="673e4-113">Return value</span></span>

<span data-ttu-id="673e4-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="673e4-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="673e4-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="673e4-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="673e4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="673e4-116">Requirements</span></span>



| <span data-ttu-id="673e4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="673e4-117">Requirement</span></span> | <span data-ttu-id="673e4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="673e4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="673e4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="673e4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="673e4-120">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="673e4-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="673e4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="673e4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="673e4-122">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="673e4-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="673e4-123">IDL</span><span class="sxs-lookup"><span data-stu-id="673e4-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="673e4-124"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="673e4-124"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="673e4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="673e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673e4-126">**IMFMediaEngineClassFactoryEx**</span><span class="sxs-lookup"><span data-stu-id="673e4-126">**IMFMediaEngineClassFactoryEx**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




