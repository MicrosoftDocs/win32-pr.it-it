---
description: Crittografa un messaggio per garantire la privacy tramite Kerberos.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: Funzione EncryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9413bc61739d67d7462e7e1257727e0401967ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233288"
---
# <a name="encryptmessage-kerberos-function"></a><span data-ttu-id="76870-103">Funzione EncryptMessage (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="76870-103">EncryptMessage (Kerberos) function</span></span>

<span data-ttu-id="76870-104">La funzione **EncryptMessage (Kerberos)** crittografa un messaggio per garantire la [*privacy*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="76870-104">The **EncryptMessage (Kerberos)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="76870-105">**EncryptMessage (Kerberos)** consente a un'applicazione di scegliere tra gli [*algoritmi di crittografia*](../secgloss/c-gly.md) supportati dal meccanismo scelto.</span><span class="sxs-lookup"><span data-stu-id="76870-105">**EncryptMessage (Kerberos)** allows an application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="76870-106">La funzione **EncryptMessage (Kerberos)** usa il [*contesto di sicurezza*](../secgloss/s-gly.md) a cui fa riferimento l'handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="76870-106">The **EncryptMessage (Kerberos)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="76870-107">Alcuni pacchetti non hanno messaggi da crittografare o decrittografare, ma forniscono un [*hash*](../secgloss/h-gly.md) di integrità che può essere controllato.</span><span class="sxs-lookup"><span data-stu-id="76870-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

> [!Note]  
> <span data-ttu-id="76870-108">**EncryptMessage (Kerberos)** e [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se è in esecuzione la crittografia di un thread e l'altro viene decrittografato.</span><span class="sxs-lookup"><span data-stu-id="76870-108">**EncryptMessage (Kerberos)** and [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="76870-109">Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.</span><span class="sxs-lookup"><span data-stu-id="76870-109">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="76870-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76870-110">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```

## <a name="parameters"></a><span data-ttu-id="76870-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="76870-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76870-112">*phContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76870-112">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76870-113">Handle per il [*contesto di sicurezza*](../secgloss/s-gly.md) da utilizzare per crittografare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="76870-113">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="76870-114">*fQOP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76870-114">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76870-115">Flag specifici del pacchetto che indicano la qualità della protezione.</span><span class="sxs-lookup"><span data-stu-id="76870-115">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="76870-116">Un [*pacchetto di sicurezza*](../secgloss/s-gly.md) può utilizzare questo parametro per abilitare la selezione degli [*algoritmi di crittografia*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="76870-116">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="76870-117">Questo parametro può essere il seguente flag.</span><span class="sxs-lookup"><span data-stu-id="76870-117">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="76870-118">Valore</span><span class="sxs-lookup"><span data-stu-id="76870-118">Value</span></span></th><th><span data-ttu-id="76870-119">Significato</span><span class="sxs-lookup"><span data-stu-id="76870-119">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="76870-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="76870-120"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="76870-121">Produrre un'intestazione o un trailer senza crittografare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="76870-121">Produce a header or trailer but do not encrypt the message.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="76870-122">KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</span><span class="sxs-lookup"><span data-stu-id="76870-122">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

</dd> <dt>

<span data-ttu-id="76870-123">*PMessage* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="76870-123">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76870-124">Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="76870-124">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="76870-125">In input, la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che possono essere di tipo SecBuffer \_ Data.</span><span class="sxs-lookup"><span data-stu-id="76870-125">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="76870-126">Il buffer contiene il messaggio da crittografare.</span><span class="sxs-lookup"><span data-stu-id="76870-126">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="76870-127">Il messaggio viene crittografato sul posto, sovrascrivendo il contenuto originale della struttura.</span><span class="sxs-lookup"><span data-stu-id="76870-127">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="76870-128">La funzione non elabora i buffer con l'attributo di sola \_ lettura SECBUFFER.</span><span class="sxs-lookup"><span data-stu-id="76870-128">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="76870-129">La lunghezza della struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che contiene il messaggio non deve essere maggiore di **cbMaximumMessage**, ottenuta dalla funzione [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG \_ attr \_ Stream \_ Sizes).</span><span class="sxs-lookup"><span data-stu-id="76870-129">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="76870-130">Le applicazioni che non usano SSL devono fornire un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) di tipo SecBuffer \_ Padding.</span><span class="sxs-lookup"><span data-stu-id="76870-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="76870-131">*MessageSeqNo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76870-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76870-132">Numero di sequenza assegnato all'applicazione di trasporto al messaggio.</span><span class="sxs-lookup"><span data-stu-id="76870-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="76870-133">Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="76870-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76870-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76870-134">Return value</span></span>

<span data-ttu-id="76870-135">Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="76870-135">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="76870-136">Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="76870-136">If the function fails, it returns one of the following error codes.</span></span>

| <span data-ttu-id="76870-137">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="76870-137">Return code</span></span>                                                                                                    | <span data-ttu-id="76870-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76870-138">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="76870-139"><dt>**SEC \_ E \_ buffer \_ troppo \_ piccolo**</dt></span><span class="sxs-lookup"><span data-stu-id="76870-139"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="76870-140">Il buffer di output è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="76870-140">The output buffer is too small.</span></span> <span data-ttu-id="76870-141">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="76870-141">For more information, see Remarks.</span></span>                                                                                                                                                                 |
| <dl> <span data-ttu-id="76870-142"><dt>**\_contesto sec \_ E \_ scaduto**</dt></span><span class="sxs-lookup"><span data-stu-id="76870-142"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="76870-143">L'applicazione fa riferimento a un contesto che è già stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="76870-143">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="76870-144">Un'applicazione scritta correttamente non dovrebbe ricevere l'errore.</span><span class="sxs-lookup"><span data-stu-id="76870-144">A properly written application should not receive this error.</span></span>                                                                                               |
| <dl> <span data-ttu-id="76870-145"><dt>**\_sistema di crittografia sec E \_ \_ \_ non valido**</dt></span><span class="sxs-lookup"><span data-stu-id="76870-145"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="76870-146">La [*crittografia*](../secgloss/c-gly.md) scelta per il [*contesto di sicurezza*](../secgloss/s-gly.md) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="76870-146">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span>                                                                                                         |
| <dl> <span data-ttu-id="76870-147"><dt>**SEC \_ E \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76870-147"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="76870-148">La memoria disponibile non è sufficiente per completare l'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="76870-148">There is not enough memory available to complete the requested action.</span></span>                                                                                                                                                             |
| <dl> <span data-ttu-id="76870-149"><dt>**\_handle sec E \_ non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76870-149"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="76870-150">Handle di contesto non valido specificato nel parametro *phContext* .</span><span class="sxs-lookup"><span data-stu-id="76870-150">A context handle that is not valid was specified in the *phContext* parameter.</span></span>                                                                                                                                                     |
| <dl> <span data-ttu-id="76870-151"><dt>**SEC \_ E \_ token non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76870-151"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="76870-152">Non \_ è stato trovato alcun buffer del tipo di dati SECBUFFER.</span><span class="sxs-lookup"><span data-stu-id="76870-152">No SECBUFFER\_DATA type buffer was found.</span></span>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="76870-153"><dt>**SEC \_ E \_ qop \_ non \_ supportati**</dt></span><span class="sxs-lookup"><span data-stu-id="76870-153"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="76870-154">Il [*contesto di sicurezza*](../secgloss/s-gly.md)non supporta né la riservatezza né l' [*integrità*](../secgloss/i-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="76870-154">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span> |

## <a name="remarks"></a><span data-ttu-id="76870-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="76870-155">Remarks</span></span>

<span data-ttu-id="76870-156">La funzione **EncryptMessage (Kerberos)** crittografa un messaggio in base al messaggio e alla [*chiave della sessione*](../secgloss/s-gly.md) da un [*contesto di sicurezza*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="76870-156">The **EncryptMessage (Kerberos)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="76870-157">Se l'applicazione di trasporto ha creato il [*contesto di sicurezza*](../secgloss/s-gly.md) per supportare il rilevamento della sequenza e il chiamante fornisce un numero di sequenza, la funzione includerà queste informazioni con il messaggio crittografato.</span><span class="sxs-lookup"><span data-stu-id="76870-157">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="76870-158">L'inclusione di queste informazioni protegge dalla riproduzione, dall'inserimento e dall'eliminazione dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="76870-158">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="76870-159">Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) incorpora il numero di sequenza passato dall'applicazione di trasporto.</span><span class="sxs-lookup"><span data-stu-id="76870-159">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

> [!Note]  
> <span data-ttu-id="76870-160">Questi buffer devono essere specificati nell'ordine indicato.</span><span class="sxs-lookup"><span data-stu-id="76870-160">These buffers must be supplied in the order shown.</span></span>

| <span data-ttu-id="76870-161">Tipo di buffer</span><span class="sxs-lookup"><span data-stu-id="76870-161">Buffer type</span></span>                           | <span data-ttu-id="76870-162">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76870-162">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76870-163">\_< intestazione del flusso SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="76870-163">SECBUFFER\_STREAM\_HEADER<</span></span>  | <span data-ttu-id="76870-164">Per uso interno.</span><span class="sxs-lookup"><span data-stu-id="76870-164">Used internally.</span></span> <span data-ttu-id="76870-165">Non è necessaria alcuna inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="76870-165">No initialization required.</span></span>                                                                       |
| <span data-ttu-id="76870-166">\_dati SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="76870-166">SECBUFFER\_DATA</span></span>            | <span data-ttu-id="76870-167">Contiene il messaggio in [*testo non crittografato*](../secgloss/s-gly.md) da crittografare.</span><span class="sxs-lookup"><span data-stu-id="76870-167">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span> |
| <span data-ttu-id="76870-168">\_trailer del flusso SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="76870-168">SECBUFFER\_STREAM\_TRAILER</span></span> | <span data-ttu-id="76870-169">Per uso interno.</span><span class="sxs-lookup"><span data-stu-id="76870-169">Used internally.</span></span> <span data-ttu-id="76870-170">Non è necessaria alcuna inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="76870-170">No initialization required.</span></span>                                                                        |
| <span data-ttu-id="76870-171">SECBUFFER \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="76870-171">SECBUFFER\_EMPTY</span></span>           | <span data-ttu-id="76870-172">Per uso interno.</span><span class="sxs-lookup"><span data-stu-id="76870-172">Used internally.</span></span> <span data-ttu-id="76870-173">Non è necessaria alcuna inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="76870-173">No initialization required.</span></span> <span data-ttu-id="76870-174">Size può essere zero.</span><span class="sxs-lookup"><span data-stu-id="76870-174">Size can be zero.</span></span>                                                      |

<span data-ttu-id="76870-175">Per ottenere prestazioni ottimali, le strutture *PMessage* devono essere allocate dalla memoria contigua.</span><span class="sxs-lookup"><span data-stu-id="76870-175">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="76870-176">**Windows XP:** Questa funzione è nota anche come **SealMessage**.</span><span class="sxs-lookup"><span data-stu-id="76870-176">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="76870-177">Le applicazioni devono ora utilizzare solo **EncryptMessage (Kerberos)** .</span><span class="sxs-lookup"><span data-stu-id="76870-177">Applications should now use **EncryptMessage (Kerberos)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="76870-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76870-178">Requirements</span></span>

| <span data-ttu-id="76870-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="76870-179">Requirement</span></span> | <span data-ttu-id="76870-180">Valore</span><span class="sxs-lookup"><span data-stu-id="76870-180">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="76870-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76870-181">Minimum supported client</span></span> | <span data-ttu-id="76870-182">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="76870-182">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="76870-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76870-183">Minimum supported server</span></span> | <span data-ttu-id="76870-184">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="76870-184">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="76870-185">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76870-185">Header</span></span>                   | <span data-ttu-id="76870-186">SSPI. h (include Security. h)</span><span class="sxs-lookup"><span data-stu-id="76870-186">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="76870-187">Libreria</span><span class="sxs-lookup"><span data-stu-id="76870-187">Library</span></span>                  | <span data-ttu-id="76870-188">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="76870-188">Secur32.lib</span></span>                               |
| <span data-ttu-id="76870-189">DLL</span><span class="sxs-lookup"><span data-stu-id="76870-189">DLL</span></span>                      | <span data-ttu-id="76870-190">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="76870-190">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="76870-191">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76870-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76870-192">Funzioni SSPI</span><span class="sxs-lookup"><span data-stu-id="76870-192">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="76870-193">**AcceptSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="76870-193">**AcceptSecurityContext (Kerberos)**</span></span>](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="76870-194">**DecryptMessage (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="76870-194">**DecryptMessage (Kerberos)**</span></span>](decryptmessage--kerberos.md)
</dt> <dt>

[<span data-ttu-id="76870-195">**InitializeSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="76870-195">**InitializeSecurityContext (Kerberos)**</span></span>](initializesecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="76870-196">**QueryContextAttributes (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="76870-196">**QueryContextAttributes (Kerberos)**</span></span>](querycontextattributes--kerberos.md)
</dt> <dt>

[<span data-ttu-id="76870-197">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="76870-197">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="76870-198">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="76870-198">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>
