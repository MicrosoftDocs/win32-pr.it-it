---
description: Ottiene un valore che indica se il tipo MIME specificato è supportato dall'origine supporto.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: 'Metodo IMFMediaSourceExtension:: IsTypeSupported'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4c2784dc4e97f96ae28ba56544a7f425de8ce742
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320684"
---
# <a name="imfmediasourceextensionistypesupported-method"></a><span data-ttu-id="2e541-103">Metodo IMFMediaSourceExtension:: IsTypeSupported</span><span class="sxs-lookup"><span data-stu-id="2e541-103">IMFMediaSourceExtension::IsTypeSupported method</span></span>

<span data-ttu-id="2e541-104">Ottiene un valore che indica se il tipo MIME specificato è supportato dall'origine supporto.</span><span class="sxs-lookup"><span data-stu-id="2e541-104">Gets a value that indicates if the specified MIME type is supported by the media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e541-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e541-105">Syntax</span></span>


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a><span data-ttu-id="2e541-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e541-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e541-107">*tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2e541-107">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e541-108">Tipo di supporto per cui verificare il supporto.</span><span class="sxs-lookup"><span data-stu-id="2e541-108">The media type to check support for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e541-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e541-109">Return value</span></span>

<span data-ttu-id="2e541-110">**true** se il tipo di supporto è supportato. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="2e541-110">**true** if the media type is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e541-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e541-111">Requirements</span></span>



| <span data-ttu-id="2e541-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e541-112">Requirement</span></span> | <span data-ttu-id="2e541-113">Valore</span><span class="sxs-lookup"><span data-stu-id="2e541-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e541-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e541-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2e541-115">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2e541-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2e541-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e541-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2e541-117">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e541-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2e541-118">IDL</span><span class="sxs-lookup"><span data-stu-id="2e541-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e541-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e541-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e541-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e541-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e541-121">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="2e541-121">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




