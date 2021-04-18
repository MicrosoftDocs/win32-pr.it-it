---
description: Utilizzato per indicare che si è verificato un errore con il buffer di origine.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: 'Metodo IMFSourceBufferNotify:: OnError'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 8b5f48c3517eb62b0a70acb9cbb28a5ecf7c90cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308478"
---
# <a name="imfsourcebuffernotifyonerror-method"></a><span data-ttu-id="53099-103">Metodo IMFSourceBufferNotify:: OnError</span><span class="sxs-lookup"><span data-stu-id="53099-103">IMFSourceBufferNotify::OnError method</span></span>

<span data-ttu-id="53099-104">Utilizzato per indicare che si è verificato un errore con il buffer di origine.</span><span class="sxs-lookup"><span data-stu-id="53099-104">Used to indicate that an error has occurred with the source buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="53099-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53099-105">Syntax</span></span>


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="53099-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="53099-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53099-107">*risorse umane* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53099-107">*hr* \[in\]</span></span>
<span data-ttu-id="53099-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="53099-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="53099-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53099-109">Return value</span></span>

<span data-ttu-id="53099-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="53099-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="53099-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53099-111">Requirements</span></span>



| <span data-ttu-id="53099-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="53099-112">Requirement</span></span> | <span data-ttu-id="53099-113">Valore</span><span class="sxs-lookup"><span data-stu-id="53099-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="53099-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53099-114">Minimum supported client</span></span><br/> | <span data-ttu-id="53099-115">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="53099-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="53099-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53099-116">Minimum supported server</span></span><br/> | <span data-ttu-id="53099-117">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="53099-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="53099-118">IDL</span><span class="sxs-lookup"><span data-stu-id="53099-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="53099-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="53099-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53099-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53099-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53099-121">**IMFSourceBufferNotify**</span><span class="sxs-lookup"><span data-stu-id="53099-121">**IMFSourceBufferNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




