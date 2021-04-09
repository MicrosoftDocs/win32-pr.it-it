---
description: Esporta il materiale delle chiavi in base allo standard RFC 5705.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: Funzione SslExportKeyingMaterial (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKeyingMaterial
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 906a7535b297f309c0c8471843ce07f43a110a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760106"
---
# <a name="sslexportkeyingmaterial-function"></a><span data-ttu-id="c3cc7-103">SslExportKeyingMaterial (funzione)</span><span class="sxs-lookup"><span data-stu-id="c3cc7-103">SslExportKeyingMaterial function</span></span>

<span data-ttu-id="c3cc7-104">Esporta il materiale delle chiavi in base allo [standard RFC 5705](https://tools.ietf.org/html/rfc5705).</span><span class="sxs-lookup"><span data-stu-id="c3cc7-104">Exports keying material per the [RFC 5705 standard](https://tools.ietf.org/html/rfc5705).</span></span> <span data-ttu-id="c3cc7-105">Questa funzione usa la funzione TLS pseudocasuale per produrre un buffer di byte del materiale per le chiavi.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-105">This function uses the TLS pseudorandom function to produce a byte buffer of keying material.</span></span> <span data-ttu-id="c3cc7-106">Accetta un riferimento all'master secret, l'etichetta ASCII distinguere, i valori casuali del client e del server e, facoltativamente, i dati del contesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-106">It takes a reference to the master secret, the disambiguating ASCII label, client and server random values, and optionally the application context data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3cc7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3cc7-107">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKeyingMaterial(
  _In_     NCRYPT_PROV_HANDLE hSslProvider,
  _In_     NCRYPT_KEY_HANDLE  hMasterKey,
  _In_     PCHAR              sLabel,
  _In_     PBYTE              pbRandoms,
  _In_     DWORD              cbRandoms,
  _In_opt_ PBYTE              pbContextValue,
  _In_     WORD               cbContextValue,
  _Out_    PBYTE              pbOutput,
  _In_     DWORD              cbOutput,
  _In_     DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c3cc7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3cc7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3cc7-109">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3cc7-109">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cc7-110">Handle dell'istanza del provider di protocollo TLS.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-110">The handle of the TLS protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="c3cc7-111">*hMasterKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3cc7-111">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cc7-112">Handle dell'oggetto chiave master che verrà usato per creare il materiale per le chiavi in br esportato.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-112">The handle of the master key object that will be used to create the keying material to br exported.</span></span>

</dd> <dt>

<span data-ttu-id="c3cc7-113">*sLabel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3cc7-113">*sLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cc7-114">stringa di etichetta ASCII con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-114">a NUL-terminated ASCII label string.</span></span> <span data-ttu-id="c3cc7-115">Schannel rimuoverà il carattere NUL di terminazione prima di passarlo alla funzione pseudocasuale.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-115">Schannel will remove the terminating NUL character before passing it to the pseudorandom function.</span></span>

</dd> <dt>

<span data-ttu-id="c3cc7-116">*pbRandoms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3cc7-116">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cc7-117">Puntatore a un buffer che contiene una concatenazione dei valori casuali del *client \_* e del *server \_ casuale* della connessione TLS.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-117">A pointer to a buffer that contains a concatenation of the *client\_random* and *server\_random* values of the TLS connection.</span></span>

</dd> <dt>

<span data-ttu-id="c3cc7-118">*cbRandoms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3cc7-118">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cc7-119">Lunghezza, in byte, del buffer *pbRandoms* .</span><span class="sxs-lookup"><span data-stu-id="c3cc7-119">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c3cc7-120">*pbContextValue* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c3cc7-120">*pbContextValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cc7-121">Puntatore a un buffer che contiene il contesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-121">A pointer to a buffer that contains the application context.</span></span> <span data-ttu-id="c3cc7-122">Se *pbContextValue* è **null**, *cbContextValue* deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-122">If *pbContextValue* is **NULL**, *cbContextValue* must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c3cc7-123">*cbContextValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3cc7-123">*cbContextValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cc7-124">Lunghezza, in byte, del buffer *pbContextValue* .</span><span class="sxs-lookup"><span data-stu-id="c3cc7-124">The length, in bytes, of the *pbContextValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c3cc7-125">*pbOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c3cc7-125">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cc7-126">Indirizzo di un buffer che riceve il materiale delle chiavi esportate.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-126">The address of a buffer that receives the exported keying material.</span></span> <span data-ttu-id="c3cc7-127">Il parametro *cbOutput* contiene la dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-127">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="c3cc7-128">Questo valore non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-128">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c3cc7-129">*cbOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3cc7-129">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cc7-130">Lunghezza, in byte, del buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="c3cc7-130">The length, in bytes, of the *pbOutput* buffer.</span></span> <span data-ttu-id="c3cc7-131">Deve essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-131">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="c3cc7-132">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3cc7-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cc7-133">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-133">Not used.</span></span> <span data-ttu-id="c3cc7-134">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-134">Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3cc7-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3cc7-135">Return value</span></span>

<span data-ttu-id="c3cc7-136">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-136">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="c3cc7-137">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-137">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="c3cc7-138">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-138">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="c3cc7-139">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3cc7-139">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="c3cc7-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3cc7-140">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="c3cc7-141"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c3cc7-141"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="c3cc7-142">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="c3cc7-142">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c3cc7-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3cc7-143">Requirements</span></span>



| <span data-ttu-id="c3cc7-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3cc7-144">Requirement</span></span> | <span data-ttu-id="c3cc7-145">Valore</span><span class="sxs-lookup"><span data-stu-id="c3cc7-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3cc7-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3cc7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c3cc7-147">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c3cc7-147">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c3cc7-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3cc7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c3cc7-149">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="c3cc7-149">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c3cc7-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c3cc7-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3cc7-151"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3cc7-151"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="c3cc7-152">DLL</span><span class="sxs-lookup"><span data-stu-id="c3cc7-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3cc7-153"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3cc7-153"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




