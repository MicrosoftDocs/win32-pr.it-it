---
description: Chiude la sessione del tasto supporto e deve essere chiamata prima del rilascio della sessione chiave.
ms.assetid: 97c6b4bd-a973-4475-a325-0373af9b54b1
title: 'Metodo IMFMediaKeySession:: Close'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Close
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 16e6efbe27c411c38dca92d12e05fe9395c4946b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320504"
---
# <a name="imfmediakeysessionclose-method"></a><span data-ttu-id="8bf80-103">Metodo IMFMediaKeySession:: Close</span><span class="sxs-lookup"><span data-stu-id="8bf80-103">IMFMediaKeySession::Close method</span></span>

<span data-ttu-id="8bf80-104">Chiude la sessione del tasto supporto e deve essere chiamata prima del rilascio della sessione chiave.</span><span class="sxs-lookup"><span data-stu-id="8bf80-104">Closes the media key session and must be called before the key session is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf80-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8bf80-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="8bf80-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bf80-106">Parameters</span></span>

<span data-ttu-id="8bf80-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8bf80-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8bf80-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bf80-108">Return value</span></span>

<span data-ttu-id="8bf80-109">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8bf80-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8bf80-110">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8bf80-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf80-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bf80-111">Requirements</span></span>



| <span data-ttu-id="8bf80-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bf80-112">Requirement</span></span> | <span data-ttu-id="8bf80-113">Valore</span><span class="sxs-lookup"><span data-stu-id="8bf80-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf80-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bf80-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf80-115">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8bf80-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8bf80-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bf80-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf80-117">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8bf80-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8bf80-118">IDL</span><span class="sxs-lookup"><span data-stu-id="8bf80-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8bf80-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8bf80-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf80-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bf80-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf80-121">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="8bf80-121">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




