---
description: Ottiene l'oggetto chiavi multimediali associato al motore multimediale o null se non è presente un oggetto chiavi multimediali.
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: 'Metodo IMFMediaEngineEME:: get_Keys'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320754"
---
# <a name="imfmediaengineemeget_keys-method"></a><span data-ttu-id="01f6e-103">Metodo IMFMediaEngineEME:: Get \_ Keys</span><span class="sxs-lookup"><span data-stu-id="01f6e-103">IMFMediaEngineEME::get\_Keys method</span></span>

<span data-ttu-id="01f6e-104">Ottiene l'oggetto chiavi multimediali associato al motore multimediale o **null** se non è presente un oggetto chiavi multimediali.</span><span class="sxs-lookup"><span data-stu-id="01f6e-104">Gets the media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

## <a name="syntax"></a><span data-ttu-id="01f6e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01f6e-105">Syntax</span></span>


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a><span data-ttu-id="01f6e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="01f6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01f6e-107">*chiavi*</span><span class="sxs-lookup"><span data-stu-id="01f6e-107">*keys*</span></span> 
</dt> <dd>

<span data-ttu-id="01f6e-108">Oggetto chiavi multimediali associato al motore multimediale o **null** se non è presente un oggetto chiavi multimediali.</span><span class="sxs-lookup"><span data-stu-id="01f6e-108">The media keys object associated with the media engine or **null** if there is not a media keys object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01f6e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01f6e-109">Return value</span></span>

<span data-ttu-id="01f6e-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="01f6e-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01f6e-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01f6e-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="01f6e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01f6e-112">Requirements</span></span>



| <span data-ttu-id="01f6e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="01f6e-113">Requirement</span></span> | <span data-ttu-id="01f6e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="01f6e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f6e-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01f6e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="01f6e-116">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="01f6e-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="01f6e-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01f6e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="01f6e-118">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="01f6e-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="01f6e-119">IDL</span><span class="sxs-lookup"><span data-stu-id="01f6e-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="01f6e-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01f6e-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01f6e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01f6e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f6e-122">**IMFMediaEngineEME**</span><span class="sxs-lookup"><span data-stu-id="01f6e-122">**IMFMediaEngineEME**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 




