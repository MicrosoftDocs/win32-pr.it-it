---
description: Calcola l'hash finale dei dati immessi dalla funzione MD5Update.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: Funzione A_SHAFinal (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324605"
---
# <a name="a_shafinal-function"></a><span data-ttu-id="4b26c-103">\_Funzione SHAFinal</span><span class="sxs-lookup"><span data-stu-id="4b26c-103">A\_SHAFinal function</span></span>

<span data-ttu-id="4b26c-104">Calcola l'hash finale dei dati immessi dalla funzione MD5Update.</span><span class="sxs-lookup"><span data-stu-id="4b26c-104">Computes the final hash of the data entered by the MD5Update function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b26c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b26c-105">Syntax</span></span>


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a><span data-ttu-id="4b26c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b26c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b26c-107">*Contesto* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4b26c-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b26c-108">Contesto SHA.</span><span class="sxs-lookup"><span data-stu-id="4b26c-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="4b26c-109">*Risultato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4b26c-109">*Result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b26c-110">Tabella hash risultante.</span><span class="sxs-lookup"><span data-stu-id="4b26c-110">The resulting hash table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b26c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b26c-111">Return value</span></span>

<span data-ttu-id="4b26c-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4b26c-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b26c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b26c-113">Remarks</span></span>

<span data-ttu-id="4b26c-114">Questa funzione è molto simile a SHAFinal, ma viene chiamata direttamente dalla libreria, anziché essere instradata tramite l'infrastruttura di crittografia.</span><span class="sxs-lookup"><span data-stu-id="4b26c-114">This function is very similar to SHAFinal, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="4b26c-115">Per ulteriori informazioni, vedere [provider NTCryptographic Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="4b26c-115">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b26c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b26c-116">Requirements</span></span>



| <span data-ttu-id="4b26c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b26c-117">Requirement</span></span> | <span data-ttu-id="4b26c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4b26c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4b26c-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b26c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4b26c-120"><dt>Sha. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b26c-120"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="4b26c-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="4b26c-121">Library</span></span><br/> | <dl> <span data-ttu-id="4b26c-122"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b26c-122"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="4b26c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4b26c-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="4b26c-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b26c-124"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
