---
description: Aggiunge dati a un oggetto hash specificato.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: Funzione A_SHAUpdate (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a0f8ac49d8221538a168ade536e55766e209d3d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324601"
---
# <a name="a_shaupdate-function"></a><span data-ttu-id="187c0-103">\_Funzione SHAUpdate</span><span class="sxs-lookup"><span data-stu-id="187c0-103">A\_SHAUpdate function</span></span>

<span data-ttu-id="187c0-104">Aggiunge dati a un oggetto hash specificato.</span><span class="sxs-lookup"><span data-stu-id="187c0-104">Adds data to a specified hash object.</span></span>

## <a name="syntax"></a><span data-ttu-id="187c0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="187c0-105">Syntax</span></span>


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="187c0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="187c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="187c0-107">*Contesto* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="187c0-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="187c0-108">Contesto SHA.</span><span class="sxs-lookup"><span data-stu-id="187c0-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="187c0-109">*Buffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="187c0-109">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="187c0-110">Tabella hash.</span><span class="sxs-lookup"><span data-stu-id="187c0-110">The hash table.</span></span>

</dd> <dt>

<span data-ttu-id="187c0-111">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="187c0-111">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="187c0-112">Dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="187c0-112">The size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="187c0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="187c0-113">Return value</span></span>

<span data-ttu-id="187c0-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="187c0-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="187c0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="187c0-115">Remarks</span></span>

<span data-ttu-id="187c0-116">Questa funzione può essere chiamata più volte per calcolare l'hash su flussi di dati lunghi o flussi di dati discontinui.</span><span class="sxs-lookup"><span data-stu-id="187c0-116">This function can be called multiple times to compute the hash on long data streams or discontinuous data streams.</span></span> <span data-ttu-id="187c0-117">Prima [**di \_**](a-shafinal.md) recuperare il valore hash, è necessario chiamare la funzione SHAFinal.</span><span class="sxs-lookup"><span data-stu-id="187c0-117">The [**A\_SHAFinal**](a-shafinal.md) function must be called before retrieving the hash value.</span></span>

<span data-ttu-id="187c0-118">Questa funzione è molto simile a SHAUpdate, ma viene chiamata direttamente dalla libreria, anziché essere instradata tramite l'infrastruttura di crittografia.</span><span class="sxs-lookup"><span data-stu-id="187c0-118">This function is very similar to SHAUpdate, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="187c0-119">Per ulteriori informazioni, vedere [provider NTCryptographic Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="187c0-119">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="187c0-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="187c0-120">Requirements</span></span>



| <span data-ttu-id="187c0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="187c0-121">Requirement</span></span> | <span data-ttu-id="187c0-122">Valore</span><span class="sxs-lookup"><span data-stu-id="187c0-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="187c0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="187c0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="187c0-124"><dt>Sha. h</dt></span><span class="sxs-lookup"><span data-stu-id="187c0-124"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="187c0-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="187c0-125">Library</span></span><br/> | <dl> <span data-ttu-id="187c0-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="187c0-126"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="187c0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="187c0-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="187c0-128"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="187c0-128"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
