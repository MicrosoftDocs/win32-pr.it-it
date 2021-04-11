---
description: Apre un handle per il provider del protocollo SSL (Secure Sockets Layer Protocol) specificato.
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: Funzione SslOpenProvider (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenProvider
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8a9ea6c97662d94fffef0c87a227d5e2ae052606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226011"
---
# <a name="sslopenprovider-function"></a><span data-ttu-id="a6183-103">SslOpenProvider (funzione)</span><span class="sxs-lookup"><span data-stu-id="a6183-103">SslOpenProvider function</span></span>

<span data-ttu-id="a6183-104">La funzione **SslOpenProvider** apre un handle per il provider del protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ) specificato.</span><span class="sxs-lookup"><span data-stu-id="a6183-104">The **SslOpenProvider** function opens a handle to the specified [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6183-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6183-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenProvider(
  _Out_ NCRYPT_PROV_HANDLE *phSslProvider,
  _In_  LPCWSTR            pszProviderName,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a6183-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6183-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6183-107">*phSslProvider* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a6183-107">*phSslProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6183-108">Indirizzo di un **handle NCRYPT \_ prov \_** in cui scrivere l'handle del provider.</span><span class="sxs-lookup"><span data-stu-id="a6183-108">The address of an **NCRYPT\_PROV\_HANDLE** in which to write the provider handle.</span></span>

<span data-ttu-id="a6183-109">Al termine dell'utilizzo dell'handle, è necessario liberarlo chiamando la funzione [**SslFreeObject**](sslfreeobject.md) .</span><span class="sxs-lookup"><span data-stu-id="a6183-109">When you have finished using the handle, you should free it by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a6183-110">*pszProviderName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6183-110">*pszProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6183-111">Puntatore a una stringa Unicode che contiene il nome del provider.</span><span class="sxs-lookup"><span data-stu-id="a6183-111">A pointer to a Unicode string that contains the provider name.</span></span> <span data-ttu-id="a6183-112">Se il valore di questo parametro è **null**, viene restituito un handle per il **\_ \_ provider MS Schannel** .</span><span class="sxs-lookup"><span data-stu-id="a6183-112">If the value of this parameter is **NULL**, a handle to the **MS\_SCHANNEL\_PROVIDER** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="a6183-113">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6183-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6183-114">Questo parametro è riservato per utilizzi futuri e deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="a6183-114">This parameter is reserved for future use, and it must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6183-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6183-115">Return value</span></span>

<span data-ttu-id="a6183-116">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="a6183-116">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="a6183-117">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a6183-117">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="a6183-118">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="a6183-118">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="a6183-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6183-119">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="a6183-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6183-120">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6183-121"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a6183-121"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="a6183-122">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="a6183-122">One of the provided handles is not valid.</span></span><br/>                      |
| <dl> <span data-ttu-id="a6183-123"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a6183-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="a6183-124">Il parametro *phSslProvider* o *ppProviderList* è **null**.</span><span class="sxs-lookup"><span data-stu-id="a6183-124">The *phSslProvider* or *ppProviderList* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="a6183-125"><dt>**Stato \_ di Nessun \_**</dt> <dt>0xC0000017L</dt> di memoria</span><span class="sxs-lookup"><span data-stu-id="a6183-125"><dt>**STATUS\_NO\_MEMORY**</dt> <dt>0xC0000017L</dt></span></span> </dl>      | <span data-ttu-id="a6183-126">La memoria disponibile non è sufficiente per allocare i buffer necessari.</span><span class="sxs-lookup"><span data-stu-id="a6183-126">Not enough memory is available to allocate necessary buffers.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="a6183-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6183-127">Requirements</span></span>



| <span data-ttu-id="a6183-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6183-128">Requirement</span></span> | <span data-ttu-id="a6183-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a6183-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6183-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6183-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a6183-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6183-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a6183-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6183-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a6183-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a6183-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a6183-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6183-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6183-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6183-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="a6183-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a6183-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6183-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6183-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

