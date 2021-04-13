---
description: Accoda il segmento multimediale specificato a IMFSourceBuffer.
ms.assetid: 824fa23d-57d9-411a-af8a-fb65dca124b2
title: 'Metodo IMFSourceBuffer:: Append'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Append
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 00c9b6a0af2e48482311a8a0e1bc39dc4ce951aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226384"
---
# <a name="imfsourcebufferappend-method"></a><span data-ttu-id="b7e12-103">Metodo IMFSourceBuffer:: Append</span><span class="sxs-lookup"><span data-stu-id="b7e12-103">IMFSourceBuffer::Append method</span></span>

<span data-ttu-id="b7e12-104">Accoda il segmento multimediale specificato a [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="b7e12-104">Appends the specified media segment to the [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e12-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7e12-105">Syntax</span></span>


```C++
HRESULT Append(
  [in] const BYTE  *pData,
  [in]       DWORD len
);
```



## <a name="parameters"></a><span data-ttu-id="b7e12-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7e12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7e12-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7e12-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e12-108">Dati multimediali da accodare.</span><span class="sxs-lookup"><span data-stu-id="b7e12-108">The media data to append.</span></span>

</dd> <dt>

<span data-ttu-id="b7e12-109">*Len* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7e12-109">*len* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7e12-110">Lunghezza dei dati multimediali archiviati in *pData*.</span><span class="sxs-lookup"><span data-stu-id="b7e12-110">The length of the media data stored in *pData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7e12-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7e12-111">Return value</span></span>

<span data-ttu-id="b7e12-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b7e12-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b7e12-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b7e12-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e12-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7e12-114">Requirements</span></span>



| <span data-ttu-id="b7e12-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7e12-115">Requirement</span></span> | <span data-ttu-id="b7e12-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b7e12-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e12-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7e12-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e12-118">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b7e12-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b7e12-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7e12-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e12-120">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7e12-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b7e12-121">IDL</span><span class="sxs-lookup"><span data-stu-id="b7e12-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7e12-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7e12-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7e12-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7e12-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e12-124">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="b7e12-124">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




