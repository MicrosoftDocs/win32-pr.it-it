---
description: Recupera il valore di una proprietà del provider specificata.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: Funzione SslGetProviderProperty (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ced0f32d45531a1220f7aae9fe0e660648e5d1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884310"
---
# <a name="sslgetproviderproperty-function"></a><span data-ttu-id="0074b-103">SslGetProviderProperty (funzione)</span><span class="sxs-lookup"><span data-stu-id="0074b-103">SslGetProviderProperty function</span></span>

<span data-ttu-id="0074b-104">La funzione **SslGetProviderProperty** Recupera il valore di una proprietà del provider specificata.</span><span class="sxs-lookup"><span data-stu-id="0074b-104">The **SslGetProviderProperty** function retrieves the value of a specified provider property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0074b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0074b-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0074b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0074b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0074b-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0074b-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0074b-108">Handle del provider di [*protocollo Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) (SSL) per il quale recuperare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="0074b-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider for which to retrieve the property.</span></span>

</dd> <dt>

<span data-ttu-id="0074b-109">*pszProperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0074b-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0074b-110">Puntatore a una stringa Unicode con terminazione null che contiene il nome della proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="0074b-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="0074b-111">*ppbOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0074b-111">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0074b-112">Indirizzo di un buffer che riceve il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="0074b-112">The address of a buffer that receives the property value.</span></span>

<span data-ttu-id="0074b-113">Il chiamante della funzione deve liberare questo buffer chiamando la funzione [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0074b-113">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="0074b-114">*pcbOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0074b-114">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0074b-115">Dimensione, in byte, del buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="0074b-115">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0074b-116">*ppEnumState* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0074b-116">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0074b-117">Indirizzo di un puntatore **void** che riceve le informazioni sullo stato di enumerazione utilizzate nelle chiamate successive a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="0074b-117">The address of a **VOID** pointer that receives enumeration state information that is used in subsequent calls to this function.</span></span> <span data-ttu-id="0074b-118">Queste informazioni hanno significato solo per il provider SSL ed è opaca per il chiamante.</span><span class="sxs-lookup"><span data-stu-id="0074b-118">This information only has meaning to the SSL provider and is opaque to the caller.</span></span> <span data-ttu-id="0074b-119">Il provider SSL usa queste informazioni per determinare l'elemento successivo nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="0074b-119">The SSL provider uses this information to determine which item is next in the enumeration.</span></span> <span data-ttu-id="0074b-120">Se la variabile a cui punta questo parametro contiene **null**, l'enumerazione viene avviata dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="0074b-120">If the variable pointed to by this parameter contains **NULL**, the enumeration is started from the beginning.</span></span>

<span data-ttu-id="0074b-121">Il chiamante della funzione deve liberare la memoria chiamando la funzione [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0074b-121">The caller of the function must free this memory by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="0074b-122">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0074b-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0074b-123">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="0074b-123">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0074b-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0074b-124">Return value</span></span>

<span data-ttu-id="0074b-125">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="0074b-125">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="0074b-126">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="0074b-126">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="0074b-127">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="0074b-127">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="0074b-128">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="0074b-128">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="0074b-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0074b-129">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0074b-130"><dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria</span><span class="sxs-lookup"><span data-stu-id="0074b-130"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="0074b-131">La memoria disponibile non è sufficiente per allocare i buffer necessari.</span><span class="sxs-lookup"><span data-stu-id="0074b-131">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="0074b-132"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0074b-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="0074b-133">Handle *hSslProvider* non valido.</span><span class="sxs-lookup"><span data-stu-id="0074b-133">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="0074b-134"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0074b-134"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="0074b-135">Uno dei parametri specificati non è valido.</span><span class="sxs-lookup"><span data-stu-id="0074b-135">One of the supplied parameters is not valid.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="0074b-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0074b-136">Requirements</span></span>



| <span data-ttu-id="0074b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="0074b-137">Requirement</span></span> | <span data-ttu-id="0074b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="0074b-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0074b-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0074b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0074b-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0074b-140">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0074b-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0074b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0074b-142">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0074b-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0074b-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0074b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="0074b-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="0074b-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="0074b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0074b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0074b-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0074b-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

