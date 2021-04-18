---
description: Incrementa il conteggio dei riferimenti a un'istanza del provider SSL (Secure Sockets Layer Protocol).
ms.assetid: 67e7b8b4-b073-4936-b1e0-3fc7c1c011a2
title: Funzione SslIncrementProviderReferenceCount (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslIncrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 862697035d978db082c303c6e1df6f2a444d8be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319387"
---
# <a name="sslincrementproviderreferencecount-function"></a><span data-ttu-id="976d1-103">SslIncrementProviderReferenceCount (funzione)</span><span class="sxs-lookup"><span data-stu-id="976d1-103">SslIncrementProviderReferenceCount function</span></span>

<span data-ttu-id="976d1-104">La funzione **SslIncrementProviderReferenceCount** incrementa il conteggio dei riferimenti a un'istanza del provider SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="976d1-104">The **SslIncrementProviderReferenceCount** function increments the reference count to a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="976d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="976d1-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslIncrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="976d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="976d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="976d1-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="976d1-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="976d1-108">Handle per l'istanza del provider del protocollo SSL.</span><span class="sxs-lookup"><span data-stu-id="976d1-108">The handle to the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="976d1-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="976d1-109">Return value</span></span>

<span data-ttu-id="976d1-110">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="976d1-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="976d1-111">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="976d1-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="976d1-112">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="976d1-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="976d1-113">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="976d1-113">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="976d1-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="976d1-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="976d1-115"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="976d1-115"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="976d1-116">Handle *hSslProvider* non valido.</span><span class="sxs-lookup"><span data-stu-id="976d1-116">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="976d1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="976d1-117">Requirements</span></span>



| <span data-ttu-id="976d1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="976d1-118">Requirement</span></span> | <span data-ttu-id="976d1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="976d1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="976d1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="976d1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="976d1-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="976d1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="976d1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="976d1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="976d1-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="976d1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="976d1-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="976d1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="976d1-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="976d1-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="976d1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="976d1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="976d1-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="976d1-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

