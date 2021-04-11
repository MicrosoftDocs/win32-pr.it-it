---
description: Decrementa i riferimenti al provider del protocollo di Secure Sockets Layer (SSL).
ms.assetid: 67bfa4b5-c02c-4a76-871d-93f3bf4e3602
title: Funzione SslDecrementProviderReferenceCount (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4d3fe072c02f22b713115dd5191b0b5e0cedbb37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967184"
---
# <a name="ssldecrementproviderreferencecount-function"></a><span data-ttu-id="c54b1-103">SslDecrementProviderReferenceCount (funzione)</span><span class="sxs-lookup"><span data-stu-id="c54b1-103">SslDecrementProviderReferenceCount function</span></span>

<span data-ttu-id="c54b1-104">La funzione **SslDecrementProviderReferenceCount** decrementa i riferimenti al provider del [*protocollo di Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="c54b1-104">The **SslDecrementProviderReferenceCount** function decrements the references to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="c54b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c54b1-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="c54b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c54b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c54b1-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c54b1-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c54b1-108">Handle dell'istanza del provider del protocollo SSL.</span><span class="sxs-lookup"><span data-stu-id="c54b1-108">The handle of the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c54b1-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c54b1-109">Return value</span></span>

<span data-ttu-id="c54b1-110">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="c54b1-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="c54b1-111">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c54b1-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="c54b1-112">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="c54b1-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="c54b1-113">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="c54b1-113">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="c54b1-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c54b1-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="c54b1-115"><dt> **Stato \_ 0xC0000008L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c54b1-115"><dt>**STATUS\_INVALID\_HANDLE** </dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="c54b1-116">Handle del provider SSL non valido.</span><span class="sxs-lookup"><span data-stu-id="c54b1-116">The SSL provider handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c54b1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c54b1-117">Requirements</span></span>



| <span data-ttu-id="c54b1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c54b1-118">Requirement</span></span> | <span data-ttu-id="c54b1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c54b1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c54b1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c54b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c54b1-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c54b1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c54b1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c54b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c54b1-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c54b1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c54b1-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c54b1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c54b1-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="c54b1-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="c54b1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c54b1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c54b1-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c54b1-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

