---
description: Consente di decrittografare un messaggio utilizzando Kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: Funzione DecryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b32968ea83ca0403a5d8dd1579c4e03f30776c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129926"
---
# <a name="decryptmessage-kerberos-function"></a><span data-ttu-id="9741e-103">Funzione DecryptMessage (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="9741e-103">DecryptMessage (Kerberos) function</span></span>

<span data-ttu-id="9741e-104">La funzione **DecryptMessage (Kerberos)** decrittografa un messaggio.</span><span class="sxs-lookup"><span data-stu-id="9741e-104">The **DecryptMessage (Kerberos)** function decrypts a message.</span></span> <span data-ttu-id="9741e-105">Alcuni pacchetti non crittografano e decrittografano i messaggi, bensì eseguono e controllano un [*hash*](../secgloss/h-gly.md)di integrità.</span><span class="sxs-lookup"><span data-stu-id="9741e-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="9741e-106">[**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) e **DecryptMessage (Kerberos)** possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se è in esecuzione la crittografia di un thread e l'altro viene decrittografato.</span><span class="sxs-lookup"><span data-stu-id="9741e-106">[**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) and **DecryptMessage (Kerberos)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="9741e-107">Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.</span><span class="sxs-lookup"><span data-stu-id="9741e-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="9741e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9741e-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="9741e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9741e-109">Parameters</span></span>

<span data-ttu-id="9741e-110">*phContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9741e-110">*phContext* \[in\]</span></span>

<span data-ttu-id="9741e-111">Handle per il [*contesto di sicurezza*](../secgloss/s-gly.md) da utilizzare per decrittografare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="9741e-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="9741e-112">*PMessage* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="9741e-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="9741e-113">Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="9741e-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="9741e-114">In input, la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che possono essere di tipo SecBuffer \_ dati.</span><span class="sxs-lookup"><span data-stu-id="9741e-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that may be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="9741e-115">Il buffer contiene il messaggio crittografato.</span><span class="sxs-lookup"><span data-stu-id="9741e-115">The buffer contains the encrypted message.</span></span> <span data-ttu-id="9741e-116">Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.</span><span class="sxs-lookup"><span data-stu-id="9741e-116">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="9741e-117">*MessageSeqNo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9741e-117">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="9741e-118">Numero di sequenza previsto dall'applicazione di trasporto, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="9741e-118">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="9741e-119">Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="9741e-119">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="9741e-120">*pfQOP* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9741e-120">*pfQOP* \[out\]</span></span>

<span data-ttu-id="9741e-121">Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.</span><span class="sxs-lookup"><span data-stu-id="9741e-121">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="9741e-122">Questo parametro può essere il seguente flag.</span><span class="sxs-lookup"><span data-stu-id="9741e-122">This parameter can be the following flag.</span></span>

| <span data-ttu-id="9741e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9741e-123">Value</span></span>                  | <span data-ttu-id="9741e-124">Significato</span><span class="sxs-lookup"><span data-stu-id="9741e-124">Meaning</span></span>                                                             |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="9741e-125">SECQOP_WRAP_NO_ENCRYPT</span><span class="sxs-lookup"><span data-stu-id="9741e-125">SECQOP_WRAP_NO_ENCRYPT</span></span> | <span data-ttu-id="9741e-126">il messaggio non è stato crittografato, ma è stata generata un'intestazione o un trailer.</span><span class="sxs-lookup"><span data-stu-id="9741e-126">he message was not encrypted, but a header or trailer was produced.</span></span> |

> [!NOTE]
> <span data-ttu-id="9741e-127">KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</span><span class="sxs-lookup"><span data-stu-id="9741e-127">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span>

## <a name="return-value"></a><span data-ttu-id="9741e-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9741e-128">Return value</span></span>

<span data-ttu-id="9741e-129">Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9741e-129">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="9741e-130">Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="9741e-130">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="9741e-131">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9741e-131">Return code</span></span>                     | <span data-ttu-id="9741e-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9741e-132">Description</span></span>                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9741e-133">**SEC \_ E \_ messaggio incompleto \_**</span><span class="sxs-lookup"><span data-stu-id="9741e-133">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="9741e-134">I dati nel buffer di input sono incompleti.</span><span class="sxs-lookup"><span data-stu-id="9741e-134">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="9741e-135">L'applicazione deve leggere più dati dal server e chiamare di nuovo [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="9741e-135">The application needs to read more data from the server and call [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) again.</span></span> |
| <span data-ttu-id="9741e-136">**SEC \_ E \_ fuori \_ \_ sequenza**</span><span class="sxs-lookup"><span data-stu-id="9741e-136">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="9741e-137">Il messaggio non è stato ricevuto nella sequenza corretta.</span><span class="sxs-lookup"><span data-stu-id="9741e-137">The message was not received in the correct sequence.</span></span>                                                                                                                            |

## <a name="remarks"></a><span data-ttu-id="9741e-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="9741e-138">Remarks</span></span>

<span data-ttu-id="9741e-139">A volte un'applicazione legge i dati dalla parte remota, tenta di decrittografarla utilizzando **DecryptMessage (Kerberos)** e rileva che **DecryptMessage (Kerberos)** ha avuto esito positivo, ma i buffer di output sono vuoti.</span><span class="sxs-lookup"><span data-stu-id="9741e-139">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Kerberos)**, and discover that **DecryptMessage (Kerberos)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="9741e-140">Si tratta di un comportamento normale che le applicazioni devono essere in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="9741e-140">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="9741e-141">Per informazioni sull'interoperabilità con GSSAPI, vedere [interoperabilità SSPI/Kerberos con GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).</span><span class="sxs-lookup"><span data-stu-id="9741e-141">For information about interoperating with GSSAPI, see [SSPI/Kerberos Interoperability with GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).</span></span>

<span data-ttu-id="9741e-142">**Windows XP:** Questa funzione è nota anche come **UnsealMessage**.</span><span class="sxs-lookup"><span data-stu-id="9741e-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="9741e-143">Le applicazioni devono ora utilizzare solo **DecryptMessage (Kerberos)** .</span><span class="sxs-lookup"><span data-stu-id="9741e-143">Applications should now use **DecryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="9741e-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9741e-144">Requirements</span></span>

| <span data-ttu-id="9741e-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="9741e-145">Requirement</span></span> | <span data-ttu-id="9741e-146">Valore</span><span class="sxs-lookup"><span data-stu-id="9741e-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="9741e-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9741e-147">Minimum supported client</span></span> | <span data-ttu-id="9741e-148">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9741e-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="9741e-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9741e-149">Minimum supported server</span></span> | <span data-ttu-id="9741e-150">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9741e-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="9741e-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9741e-151">Header</span></span>                   | <span data-ttu-id="9741e-152">SSPI. h (include Security. h)</span><span class="sxs-lookup"><span data-stu-id="9741e-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="9741e-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="9741e-153">Library</span></span>                  | <span data-ttu-id="9741e-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="9741e-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="9741e-155">DLL</span><span class="sxs-lookup"><span data-stu-id="9741e-155">DLL</span></span>                      | <span data-ttu-id="9741e-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="9741e-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="9741e-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9741e-157">See also</span></span>

- [<span data-ttu-id="9741e-158">Funzioni SSPI</span><span class="sxs-lookup"><span data-stu-id="9741e-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="9741e-159">**EncryptMessage (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="9741e-159">**EncryptMessage (Kerberos)**</span></span>](encryptmessage--kerberos.md)
- [<span data-ttu-id="9741e-160">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="9741e-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="9741e-161">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="9741e-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
