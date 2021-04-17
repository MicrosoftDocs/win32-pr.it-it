---
description: Restituisce una matrice di provider di protocollo SSL (installated Secure Sockets Layer Protocol).
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: Funzione SslEnumProtocolProviders (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 94c8648950af20a97bcc34b614aee0d0f716b043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234009"
---
# <a name="sslenumprotocolproviders-function"></a><span data-ttu-id="d884e-103">SslEnumProtocolProviders (funzione)</span><span class="sxs-lookup"><span data-stu-id="d884e-103">SslEnumProtocolProviders function</span></span>

<span data-ttu-id="d884e-104">La funzione **SslEnumProtocolProviders** restituisce una matrice di provider di protocollo SSL (installated [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="d884e-104">The **SslEnumProtocolProviders** function returns an array of installed [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d884e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d884e-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d884e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d884e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d884e-107">*pdwProviderCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d884e-107">*pdwProviderCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d884e-108">Puntatore a un valore **DWORD** per ricevere il numero di provider di protocollo restituiti.</span><span class="sxs-lookup"><span data-stu-id="d884e-108">A pointer to a **DWORD** value to receive the number of protocol providers returned.</span></span>

</dd> <dt>

<span data-ttu-id="d884e-109">*ppProviderList* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d884e-109">*ppProviderList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d884e-110">Puntatore a un buffer che riceve la matrice di strutture [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) .</span><span class="sxs-lookup"><span data-stu-id="d884e-110">A pointer to a buffer that receives the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures.</span></span>

</dd> <dt>

<span data-ttu-id="d884e-111">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d884e-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d884e-112">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="d884e-112">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d884e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d884e-113">Return value</span></span>

<span data-ttu-id="d884e-114">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="d884e-114">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="d884e-115">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="d884e-115">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="d884e-116">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="d884e-116">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="d884e-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="d884e-117">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="d884e-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d884e-118">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d884e-119"><dt>**Nte \_ \_Flag non validi**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="d884e-119"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="d884e-120">Il parametro *dwFlags* è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="d884e-120">The *dwFlags* parameter is not zero.</span></span><br/>                              |
| <dl> <span data-ttu-id="d884e-121"><dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria</span><span class="sxs-lookup"><span data-stu-id="d884e-121"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="d884e-122">La memoria disponibile non è sufficiente per allocare i buffer necessari.</span><span class="sxs-lookup"><span data-stu-id="d884e-122">Not enough memory is available to allocate necessary buffers.</span></span><br/>     |
| <dl> <span data-ttu-id="d884e-123"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d884e-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="d884e-124">Il parametro *pdwProviderCount* o *ppProviderList* è **null**.</span><span class="sxs-lookup"><span data-stu-id="d884e-124">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d884e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="d884e-125">Remarks</span></span>

<span data-ttu-id="d884e-126">Al termine dell'utilizzo della matrice di strutture [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) , chiamare la funzione [**SslFreeBuffer**](sslfreebuffer.md) per liberare la matrice.</span><span class="sxs-lookup"><span data-stu-id="d884e-126">When you have finished using the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures, call the [**SslFreeBuffer**](sslfreebuffer.md) function to free the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="d884e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d884e-127">Requirements</span></span>



| <span data-ttu-id="d884e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d884e-128">Requirement</span></span> | <span data-ttu-id="d884e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d884e-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d884e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d884e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d884e-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d884e-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d884e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d884e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d884e-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d884e-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d884e-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d884e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d884e-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="d884e-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="d884e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d884e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d884e-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d884e-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

