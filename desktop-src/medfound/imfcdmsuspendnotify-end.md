---
description: La sospensione effettiva sta per verificarsi e non verrà più effettuata alcuna chiamata al modulo di decrittografia del contenuto (CDM).
ms.assetid: 7a319fbb-9757-45da-8a8b-51dd48f08464
title: 'Metodo IMFCdmSuspendNotify:: end'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.End
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 71843b53fa85fded646fe71f2caa463a71c9415f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310830"
---
# <a name="imfcdmsuspendnotifyend-method"></a><span data-ttu-id="4ec7b-103">Metodo IMFCdmSuspendNotify:: end</span><span class="sxs-lookup"><span data-stu-id="4ec7b-103">IMFCdmSuspendNotify::End method</span></span>

<span data-ttu-id="4ec7b-104">La sospensione effettiva sta per verificarsi e non verrà più effettuata alcuna chiamata al modulo di decrittografia del contenuto (CDM).</span><span class="sxs-lookup"><span data-stu-id="4ec7b-104">The actual suspend is about to occur and no more calls will be made into the Content Decryption Module (CDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ec7b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ec7b-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="4ec7b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ec7b-106">Parameters</span></span>

<span data-ttu-id="4ec7b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4ec7b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ec7b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ec7b-108">Return value</span></span>

<span data-ttu-id="4ec7b-109">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4ec7b-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4ec7b-110">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4ec7b-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ec7b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ec7b-111">Requirements</span></span>



| <span data-ttu-id="4ec7b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ec7b-112">Requirement</span></span> | <span data-ttu-id="4ec7b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4ec7b-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ec7b-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ec7b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4ec7b-115">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4ec7b-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4ec7b-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ec7b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4ec7b-117">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4ec7b-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4ec7b-118">IDL</span><span class="sxs-lookup"><span data-stu-id="4ec7b-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ec7b-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ec7b-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ec7b-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ec7b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec7b-121">**IMFCdmSuspendNotify**</span><span class="sxs-lookup"><span data-stu-id="4ec7b-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




