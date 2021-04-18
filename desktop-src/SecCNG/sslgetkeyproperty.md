---
description: Recupera il valore di una proprietà denominata per un oggetto chiave del provider SSL (Secure Sockets Layer Protocol).
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: Funzione SslGetKeyProperty (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetKeyProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 42952b76bfb46eeeb31b9f76b1f677e7b3b8e3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316720"
---
# <a name="sslgetkeyproperty-function"></a><span data-ttu-id="8ecc7-103">SslGetKeyProperty (funzione)</span><span class="sxs-lookup"><span data-stu-id="8ecc7-103">SslGetKeyProperty function</span></span>

<span data-ttu-id="8ecc7-104">La funzione **SslGetKeyProperty** Recupera il valore di una proprietà denominata per un oggetto chiave del provider SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="8ecc7-104">The **SslGetKeyProperty** function retrieves the value of a named property for a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider key object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ecc7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ecc7-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetKeyProperty(
  _In_  NCRYPT_KEY_HANDLE hKey,
  _In_  LPCWSTR           pszProperty,
  _Out_ PBYTE             ppbOutput,
  _Out_ DWORD             *pcbOutput,
  _In_  DWORD             dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8ecc7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ecc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ecc7-107">*HKEY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ecc7-107">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ecc7-108">Handle del provider SSL.</span><span class="sxs-lookup"><span data-stu-id="8ecc7-108">The handle of the SSL provider.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc7-109">*pszProperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ecc7-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ecc7-110">Puntatore a una stringa Unicode con terminazione null che contiene il nome della proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="8ecc7-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span> <span data-ttu-id="8ecc7-111">Può essere uno degli [**identificatori di proprietà di archiviazione chiavi**](key-storage-property-identifiers.md) predefiniti o un identificatore di proprietà personalizzato.</span><span class="sxs-lookup"><span data-stu-id="8ecc7-111">This can be one of the predefined [**Key Storage Property Identifiers**](key-storage-property-identifiers.md) or a custom property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc7-112">*ppbOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ecc7-112">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ecc7-113">Puntatore a un buffer che riceve il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8ecc7-113">A pointer to a buffer that receives the property value.</span></span> <span data-ttu-id="8ecc7-114">Il chiamante della funzione deve liberare questo buffer chiamando la funzione [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8ecc7-114">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc7-115">*pcbOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ecc7-115">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ecc7-116">Dimensione, in byte, del buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="8ecc7-116">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc7-117">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ecc7-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ecc7-118">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="8ecc7-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ecc7-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ecc7-119">Return value</span></span>

<span data-ttu-id="8ecc7-120">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="8ecc7-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="8ecc7-121">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="8ecc7-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="8ecc7-122">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="8ecc7-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="8ecc7-123">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ecc7-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="8ecc7-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ecc7-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="8ecc7-125"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8ecc7-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="8ecc7-126">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="8ecc7-126">One of the provided handles is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="8ecc7-127"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8ecc7-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="8ecc7-128">Uno dei parametri specificati non è valido.</span><span class="sxs-lookup"><span data-stu-id="8ecc7-128">One of the supplied parameters is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8ecc7-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ecc7-129">Requirements</span></span>



| <span data-ttu-id="8ecc7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ecc7-130">Requirement</span></span> | <span data-ttu-id="8ecc7-131">Valore</span><span class="sxs-lookup"><span data-stu-id="8ecc7-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ecc7-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ecc7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8ecc7-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ecc7-133">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8ecc7-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ecc7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8ecc7-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8ecc7-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8ecc7-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ecc7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ecc7-137"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ecc7-137"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="8ecc7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8ecc7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ecc7-139"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ecc7-139"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

