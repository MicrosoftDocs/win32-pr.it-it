---
description: Avvia l'hashing di un flusso di dati.
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: Funzione A_SHAInit (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAInit
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 831c86b02c946896014fa9eec02270f2e963e484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324602"
---
# <a name="a_shainit-function"></a><span data-ttu-id="b6505-103">\_Funzione SHAInit</span><span class="sxs-lookup"><span data-stu-id="b6505-103">A\_SHAInit function</span></span>

<span data-ttu-id="b6505-104">Avvia l'hashing di un flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="b6505-104">Initiates the hashing of a stream of data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6505-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6505-105">Syntax</span></span>


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a><span data-ttu-id="b6505-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6505-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6505-107">*Contesto* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b6505-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6505-108">Contesto SHA.</span><span class="sxs-lookup"><span data-stu-id="b6505-108">The SHA context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6505-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6505-109">Return value</span></span>

<span data-ttu-id="b6505-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b6505-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6505-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6505-111">Remarks</span></span>

<span data-ttu-id="b6505-112">Questa funzione è molto simile a SHAInit, ma viene chiamata direttamente dalla libreria, anziché essere instradata tramite l'infrastruttura di crittografia.</span><span class="sxs-lookup"><span data-stu-id="b6505-112">This function is very similar to SHAInit, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="b6505-113">Per ulteriori informazioni, vedere [provider NTCryptographic Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="b6505-113">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6505-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6505-114">Requirements</span></span>



| <span data-ttu-id="b6505-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6505-115">Requirement</span></span> | <span data-ttu-id="b6505-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b6505-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b6505-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6505-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b6505-118"><dt>Sha. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6505-118"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="b6505-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="b6505-119">Library</span></span><br/> | <dl> <span data-ttu-id="b6505-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6505-120"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="b6505-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b6505-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="b6505-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6505-122"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
