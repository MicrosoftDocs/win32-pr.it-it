---
description: Calcola il blocco di chiavi utilizzato da Extensible Authentication Protocol (EAP).
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: Funzione SslComputeEapKeyBlock (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: d46c1284b208975126067ff295507b51def9133b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310767"
---
# <a name="sslcomputeeapkeyblock-function"></a><span data-ttu-id="ace03-103">SslComputeEapKeyBlock (funzione)</span><span class="sxs-lookup"><span data-stu-id="ace03-103">SslComputeEapKeyBlock function</span></span>

<span data-ttu-id="ace03-104">La funzione **SslComputeEapKeyBlock** calcola il blocco di chiave utilizzato da Extensible Authentication Protocol (EAP).</span><span class="sxs-lookup"><span data-stu-id="ace03-104">The **SslComputeEapKeyBlock** function computes the key block used by the Extensible Authentication Protocol (EAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="ace03-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ace03-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ace03-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ace03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace03-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ace03-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace03-108">Handle dell'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="ace03-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="ace03-109">*hMasterKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ace03-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace03-110">Handle dell'oggetto [*chiave master*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="ace03-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="ace03-111">*pbRandoms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ace03-111">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace03-112">Puntatore a un buffer che contiene una concatenazione dei valori casuali del client \_ e del server \_ casuale della sessione SSL.</span><span class="sxs-lookup"><span data-stu-id="ace03-112">A pointer to a buffer that contains a concatenation of the client\_random and server\_random values of the SSL session.</span></span>

</dd> <dt>

<span data-ttu-id="ace03-113">*cbRandoms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ace03-113">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace03-114">Lunghezza, in byte, del buffer *pbRandoms* .</span><span class="sxs-lookup"><span data-stu-id="ace03-114">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ace03-115">*pbOutput* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ace03-115">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ace03-116">Indirizzo di un buffer che riceve il BLOB della chiave.</span><span class="sxs-lookup"><span data-stu-id="ace03-116">The address of a buffer that receives the key BLOB.</span></span> <span data-ttu-id="ace03-117">Il parametro *cbOutput* contiene la dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="ace03-117">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="ace03-118">Se questo parametro è **null**, questa funzione inserisce la dimensione richiesta, in byte, nel **valore DWORD** a cui fa riferimento il parametro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="ace03-118">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ace03-119">*cbOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ace03-119">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace03-120">Lunghezza, in byte, del buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="ace03-120">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ace03-121">*pcbResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ace03-121">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ace03-122">Puntatore a un valore **DWORD** che specifica la lunghezza, in byte, dell'hash scritto nel buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="ace03-122">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ace03-123">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ace03-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace03-124">Impostare su **NCRYPT \_ SSL \_ server \_ flag** per indicare che si tratta di una chiamata al server.</span><span class="sxs-lookup"><span data-stu-id="ace03-124">Set to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace03-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ace03-125">Return value</span></span>

<span data-ttu-id="ace03-126">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="ace03-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="ace03-127">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="ace03-127">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="ace03-128">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="ace03-128">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="ace03-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ace03-129">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="ace03-130"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ace03-130"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="ace03-131">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="ace03-131">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ace03-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ace03-132">Requirements</span></span>



| <span data-ttu-id="ace03-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ace03-133">Requirement</span></span> | <span data-ttu-id="ace03-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ace03-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace03-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ace03-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ace03-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ace03-136">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ace03-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ace03-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ace03-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ace03-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ace03-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ace03-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ace03-140"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="ace03-140"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="ace03-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ace03-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ace03-142"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ace03-142"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

