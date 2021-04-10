---
description: Utilizzato per liberare la memoria allocata da una delle funzioni del provider di protocollo Secure Sockets Layer (SSL).
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: Funzione SslFreeBuffer (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeBuffer
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bced83b52ddf37266f64ae0c2b8919902f30fff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058314"
---
# <a name="sslfreebuffer-function"></a><span data-ttu-id="7ce90-103">SslFreeBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="7ce90-103">SslFreeBuffer function</span></span>

<span data-ttu-id="7ce90-104">La funzione **SslFreeBuffer** viene utilizzata per liberare la memoria allocata da una delle funzioni del provider di protocollo SSL ( [*Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="7ce90-104">The **SslFreeBuffer** function is used to free memory that was allocated by one of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ce90-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ce90-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a><span data-ttu-id="7ce90-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ce90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ce90-107">*pvInput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ce90-107">*pvInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce90-108">Puntatore al buffer di memoria da liberare.</span><span class="sxs-lookup"><span data-stu-id="7ce90-108">A pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ce90-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ce90-109">Return value</span></span>

<span data-ttu-id="7ce90-110">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="7ce90-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="7ce90-111">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="7ce90-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="7ce90-112">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="7ce90-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="7ce90-113">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ce90-113">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="7ce90-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ce90-114">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7ce90-115"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7ce90-115"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="7ce90-116">Il parametro *pdwProviderCount* o *ppProviderList* è **null**.</span><span class="sxs-lookup"><span data-stu-id="7ce90-116">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7ce90-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ce90-117">Requirements</span></span>



| <span data-ttu-id="7ce90-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ce90-118">Requirement</span></span> | <span data-ttu-id="7ce90-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7ce90-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ce90-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ce90-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7ce90-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ce90-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7ce90-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ce90-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7ce90-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ce90-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7ce90-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ce90-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ce90-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ce90-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="7ce90-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7ce90-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ce90-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ce90-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

