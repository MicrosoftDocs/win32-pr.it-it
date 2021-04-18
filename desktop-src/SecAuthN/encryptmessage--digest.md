---
description: Crittografa un messaggio per garantire la privacy tramite digest.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: Funzione EncryptMessage (digest) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13bcaa5b91f165321d03e229416741b90a978dc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305865"
---
# <a name="encryptmessage-digest-function"></a><span data-ttu-id="a0291-103">Funzione EncryptMessage (digest)</span><span class="sxs-lookup"><span data-stu-id="a0291-103">EncryptMessage (Digest) function</span></span>

<span data-ttu-id="a0291-104">La funzione **EncryptMessage (digest)** crittografa un messaggio per garantire la [*privacy*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a0291-104">The **EncryptMessage (Digest)** function encrypts a message to provide [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="a0291-105">**EncryptMessage (digest)** consente all'applicazione di scegliere tra gli [*algoritmi di crittografia*](../secgloss/c-gly.md) supportati dal meccanismo scelto.</span><span class="sxs-lookup"><span data-stu-id="a0291-105">**EncryptMessage (Digest)** allows the application to choose among [*cryptographic algorithms*](../secgloss/c-gly.md) supported by the chosen mechanism.</span></span> <span data-ttu-id="a0291-106">La funzione **EncryptMessage (digest)** usa il [*contesto di sicurezza*](../secgloss/s-gly.md) a cui fa riferimento l'handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="a0291-106">The **EncryptMessage (Digest)** function uses the [*security context*](../secgloss/s-gly.md) referenced by the context handle.</span></span> <span data-ttu-id="a0291-107">Alcuni pacchetti non hanno messaggi da crittografare o decrittografare, ma forniscono un [*hash*](../secgloss/h-gly.md) di integrità che può essere controllato.</span><span class="sxs-lookup"><span data-stu-id="a0291-107">Some packages do not have messages to be encrypted or decrypted but rather provide an integrity [*hash*](../secgloss/h-gly.md) that can be checked.</span></span>

<span data-ttu-id="a0291-108">Questa funzione è disponibile solo come meccanismo SASL.</span><span class="sxs-lookup"><span data-stu-id="a0291-108">This function is available as a SASL mechanism only.</span></span>

> [!Note]  
> <span data-ttu-id="a0291-109">**EncryptMessage (digest)** e [**DecryptMessage (digest)**](decryptmessage--digest.md) possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se un thread esegue la crittografia e l'altro esegue la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="a0291-109">**EncryptMessage (Digest)** and [**DecryptMessage (Digest)**](decryptmessage--digest.md) can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="a0291-110">Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.</span><span class="sxs-lookup"><span data-stu-id="a0291-110">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a0291-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0291-111">Syntax</span></span>


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
);
```



## <a name="parameters"></a><span data-ttu-id="a0291-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0291-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0291-113">*phContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0291-113">*phContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0291-114">Handle per il [*contesto di sicurezza*](../secgloss/s-gly.md) da utilizzare per crittografare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="a0291-114">A handle to the [*security context*](../secgloss/s-gly.md) to be used to encrypt the message.</span></span>

</dd> <dt>

<span data-ttu-id="a0291-115">*fQOP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0291-115">*fQOP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0291-116">Flag specifici del pacchetto che indicano la qualità della protezione.</span><span class="sxs-lookup"><span data-stu-id="a0291-116">Package-specific flags that indicate the quality of protection.</span></span> <span data-ttu-id="a0291-117">Un [*pacchetto di sicurezza*](../secgloss/s-gly.md) può utilizzare questo parametro per abilitare la selezione degli [*algoritmi di crittografia*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a0291-117">A [*security package*](../secgloss/s-gly.md) can use this parameter to enable the selection of [*cryptographic algorithms*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="a0291-118">Quando si utilizza SSP digest, questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="a0291-118">When using the Digest SSP, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a0291-119">*PMessage* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a0291-119">*pMessage* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0291-120">Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="a0291-120">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="a0291-121">In input, la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che possono essere di tipo SecBuffer \_ Data.</span><span class="sxs-lookup"><span data-stu-id="a0291-121">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures that can be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="a0291-122">Il buffer contiene il messaggio da crittografare.</span><span class="sxs-lookup"><span data-stu-id="a0291-122">That buffer contains the message to be encrypted.</span></span> <span data-ttu-id="a0291-123">Il messaggio viene crittografato sul posto, sovrascrivendo il contenuto originale della struttura.</span><span class="sxs-lookup"><span data-stu-id="a0291-123">The message is encrypted in place, overwriting the original contents of the structure.</span></span>

<span data-ttu-id="a0291-124">La funzione non elabora i buffer con l'attributo di sola \_ lettura SECBUFFER.</span><span class="sxs-lookup"><span data-stu-id="a0291-124">The function does not process buffers with the SECBUFFER\_READONLY attribute.</span></span>

<span data-ttu-id="a0291-125">La lunghezza della struttura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) che contiene il messaggio non deve essere maggiore di **cbMaximumMessage**, ottenuta dalla funzione [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) (SECPKG \_ attr \_ Stream \_ Sizes).</span><span class="sxs-lookup"><span data-stu-id="a0291-125">The length of the [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structure that contains the message must be no greater than **cbMaximumMessage**, which is obtained from the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG\_ATTR\_STREAM\_SIZES) function.</span></span>

<span data-ttu-id="a0291-126">Quando si usa il provider di servizi condivisi del digest, è necessario che sia presente un secondo buffer di tipo SECBUFFER \_ Padding o sec \_ buffer \_ data per contenere le informazioni sulla [*firma*](../secgloss/d-gly.md#_security_digital_signature_gly) .</span><span class="sxs-lookup"><span data-stu-id="a0291-126">When using the Digest SSP, there must be a second buffer of type SECBUFFER\_PADDING or SEC\_BUFFER\_DATA to hold [*signature*](../secgloss/d-gly.md#_security_digital_signature_gly) information.</span></span> <span data-ttu-id="a0291-127">Per ottenere le dimensioni del buffer di output, chiamare la funzione [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) e specificare SECPKG \_ attr \_ sizes.</span><span class="sxs-lookup"><span data-stu-id="a0291-127">To get the size of the output buffer, call the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specify SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="a0291-128">La funzione restituirà una struttura di [**\_ dimensioni SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .</span><span class="sxs-lookup"><span data-stu-id="a0291-128">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="a0291-129">La dimensione del buffer di output è la somma dei valori nei membri **cbMaxSignature** e **cbBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="a0291-129">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

<span data-ttu-id="a0291-130">Le applicazioni che non usano SSL devono fornire un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) di tipo SecBuffer \_ Padding.</span><span class="sxs-lookup"><span data-stu-id="a0291-130">Applications that do not use SSL must supply a [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) of type SECBUFFER\_PADDING.</span></span>

</dd> <dt>

<span data-ttu-id="a0291-131">*MessageSeqNo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0291-131">*MessageSeqNo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0291-132">Numero di sequenza assegnato all'applicazione di trasporto al messaggio.</span><span class="sxs-lookup"><span data-stu-id="a0291-132">The sequence number that the transport application assigned to the message.</span></span> <span data-ttu-id="a0291-133">Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a0291-133">If the transport application does not maintain sequence numbers, this parameter must be zero.</span></span>

<span data-ttu-id="a0291-134">Quando si utilizza SSP digest, questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="a0291-134">When using the Digest SSP, this parameter must be set to zero.</span></span> <span data-ttu-id="a0291-135">SSP digest gestisce internamente i numeri di sequenza.</span><span class="sxs-lookup"><span data-stu-id="a0291-135">The Digest SSP manages sequence numbering internally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0291-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0291-136">Return value</span></span>

<span data-ttu-id="a0291-137">Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0291-137">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="a0291-138">Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="a0291-138">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="a0291-139">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a0291-139">Return code</span></span>                                                                                                    | <span data-ttu-id="a0291-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0291-140">Description</span></span>                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a0291-141"><dt>**SEC \_ E \_ buffer \_ troppo \_ piccolo**</dt></span><span class="sxs-lookup"><span data-stu-id="a0291-141"><dt>**SEC\_E\_BUFFER\_TOO\_SMALL**</dt></span></span> </dl>      | <span data-ttu-id="a0291-142">Il buffer di output è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="a0291-142">The output buffer is too small.</span></span> <span data-ttu-id="a0291-143">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a0291-143">For more information, see Remarks.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="a0291-144"><dt>**\_contesto sec \_ E \_ scaduto**</dt></span><span class="sxs-lookup"><span data-stu-id="a0291-144"><dt>**SEC\_E\_CONTEXT\_EXPIRED**</dt></span></span> </dl>        | <span data-ttu-id="a0291-145">L'applicazione fa riferimento a un contesto che è già stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="a0291-145">The application is referencing a context that has already been closed.</span></span> <span data-ttu-id="a0291-146">Un'applicazione scritta correttamente non dovrebbe ricevere l'errore.</span><span class="sxs-lookup"><span data-stu-id="a0291-146">A properly written application should not receive this error.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="a0291-147"><dt>**\_sistema di crittografia sec E \_ \_ \_ non valido**</dt></span><span class="sxs-lookup"><span data-stu-id="a0291-147"><dt>**SEC\_E\_CRYPTO\_SYSTEM\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="a0291-148">La [*crittografia*](../secgloss/c-gly.md) scelta per il [*contesto di sicurezza*](../secgloss/s-gly.md) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a0291-148">The [*cipher*](../secgloss/c-gly.md) chosen for the [*security context*](../secgloss/s-gly.md) is not supported.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="a0291-149"><dt>**SEC \_ E \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a0291-149"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="a0291-150">La memoria disponibile non è sufficiente per completare l'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="a0291-150">There is not enough memory available to complete the requested action.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="a0291-151"><dt>**\_handle sec E \_ non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a0291-151"><dt>**SEC\_E\_INVALID\_HANDLE**</dt></span></span> </dl>         | <span data-ttu-id="a0291-152">Handle di contesto non valido specificato nel parametro *phContext* .</span><span class="sxs-lookup"><span data-stu-id="a0291-152">A context handle that is not valid was specified in the *phContext* parameter.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="a0291-153"><dt>**SEC \_ E \_ token non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a0291-153"><dt>**SEC\_E\_INVALID\_TOKEN**</dt></span></span> </dl>          | <span data-ttu-id="a0291-154">Non \_ è stato trovato alcun buffer del tipo di dati SECBUFFER.</span><span class="sxs-lookup"><span data-stu-id="a0291-154">No SECBUFFER\_DATA type buffer was found.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="a0291-155"><dt>**SEC \_ E \_ qop \_ non \_ supportati**</dt></span><span class="sxs-lookup"><span data-stu-id="a0291-155"><dt>**SEC\_E\_QOP\_NOT\_SUPPORTED**</dt></span></span> </dl>     | <span data-ttu-id="a0291-156">Il [*contesto di sicurezza*](../secgloss/s-gly.md)non supporta né la riservatezza né l' [*integrità*](../secgloss/i-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a0291-156">Neither confidentiality nor [*integrity*](../secgloss/i-gly.md) are supported by the [*security context*](../secgloss/s-gly.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a0291-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0291-157">Remarks</span></span>

<span data-ttu-id="a0291-158">La funzione **EncryptMessage (digest)** crittografa un messaggio in base al messaggio e alla [*chiave della sessione*](../secgloss/s-gly.md) da un [*contesto di sicurezza*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a0291-158">The **EncryptMessage (Digest)** function encrypts a message based on the message and the [*session key*](../secgloss/s-gly.md) from a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="a0291-159">Se l'applicazione di trasporto ha creato il [*contesto di sicurezza*](../secgloss/s-gly.md) per supportare il rilevamento della sequenza e il chiamante fornisce un numero di sequenza, la funzione includerà queste informazioni con il messaggio crittografato.</span><span class="sxs-lookup"><span data-stu-id="a0291-159">If the transport application created the [*security context*](../secgloss/s-gly.md) to support sequence detection and the caller provides a sequence number, the function includes this information with the encrypted message.</span></span> <span data-ttu-id="a0291-160">L'inclusione di queste informazioni protegge dalla riproduzione, dall'inserimento e dall'eliminazione dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="a0291-160">Including this information protects against replay, insertion, and suppression of messages.</span></span> <span data-ttu-id="a0291-161">Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) incorpora il numero di sequenza passato dall'applicazione di trasporto.</span><span class="sxs-lookup"><span data-stu-id="a0291-161">The [*security package*](../secgloss/s-gly.md) incorporates the sequence number passed down from the transport application.</span></span>

<span data-ttu-id="a0291-162">Quando si usa il provider di servizi condivisi del digest, ottenere le dimensioni del buffer di output chiamando la funzione [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) e specificando SECPKG \_ attr \_ sizes.</span><span class="sxs-lookup"><span data-stu-id="a0291-162">When you use the Digest SSP, get the size of the output buffer by calling the [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) function and specifying SECPKG\_ATTR\_SIZES.</span></span> <span data-ttu-id="a0291-163">La funzione restituirà una struttura di [**\_ dimensioni SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) .</span><span class="sxs-lookup"><span data-stu-id="a0291-163">The function will return a [**SecPkgContext\_Sizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) structure.</span></span> <span data-ttu-id="a0291-164">La dimensione del buffer di output è la somma dei valori nei membri **cbMaxSignature** e **cbBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="a0291-164">The size of the output buffer is the sum of the values in the **cbMaxSignature** and **cbBlockSize** members.</span></span>

> [!Note]  
> <span data-ttu-id="a0291-165">Questi buffer devono essere specificati nell'ordine indicato.</span><span class="sxs-lookup"><span data-stu-id="a0291-165">These buffers must be supplied in the order shown.</span></span>

 



| <span data-ttu-id="a0291-166">Tipo di buffer</span><span class="sxs-lookup"><span data-stu-id="a0291-166">Buffer type</span></span>                           | <span data-ttu-id="a0291-167">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0291-167">Description</span></span>                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0291-168">\_intestazione del flusso SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="a0291-168">SECBUFFER\_STREAM\_HEADER</span></span><br/>  | <span data-ttu-id="a0291-169">Per uso interno.</span><span class="sxs-lookup"><span data-stu-id="a0291-169">Used internally.</span></span> <span data-ttu-id="a0291-170">Non è necessaria alcuna inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="a0291-170">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="a0291-171">\_dati SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="a0291-171">SECBUFFER\_DATA</span></span><br/>            | <span data-ttu-id="a0291-172">Contiene il messaggio in [*testo non crittografato*](../secgloss/s-gly.md) da crittografare.</span><span class="sxs-lookup"><span data-stu-id="a0291-172">Contains the [*plaintext*](../secgloss/s-gly.md) message to be encrypted.</span></span><br/> |
| <span data-ttu-id="a0291-173">\_trailer del flusso SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="a0291-173">SECBUFFER\_STREAM\_TRAILER</span></span><br/> | <span data-ttu-id="a0291-174">Per uso interno.</span><span class="sxs-lookup"><span data-stu-id="a0291-174">Used internally.</span></span> <span data-ttu-id="a0291-175">Non è necessaria alcuna inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="a0291-175">No initialization required.</span></span><br/>                                                                        |
| <span data-ttu-id="a0291-176">SECBUFFER \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="a0291-176">SECBUFFER\_EMPTY</span></span><br/>           | <span data-ttu-id="a0291-177">Per uso interno.</span><span class="sxs-lookup"><span data-stu-id="a0291-177">Used internally.</span></span> <span data-ttu-id="a0291-178">Non è necessaria alcuna inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="a0291-178">No initialization required.</span></span> <span data-ttu-id="a0291-179">Size può essere zero.</span><span class="sxs-lookup"><span data-stu-id="a0291-179">Size can be zero.</span></span><br/>                                                      |



 

<span data-ttu-id="a0291-180">Per ottenere prestazioni ottimali, le strutture *PMessage* devono essere allocate dalla memoria contigua.</span><span class="sxs-lookup"><span data-stu-id="a0291-180">For optimal performance, the *pMessage* structures should be allocated from contiguous memory.</span></span>

<span data-ttu-id="a0291-181">**Windows XP:** Questa funzione è nota anche come **SealMessage**.</span><span class="sxs-lookup"><span data-stu-id="a0291-181">**Windows XP:** This function was also known as **SealMessage**.</span></span> <span data-ttu-id="a0291-182">Le applicazioni devono ora usare solo **EncryptMessage (digest)** .</span><span class="sxs-lookup"><span data-stu-id="a0291-182">Applications should now use **EncryptMessage (Digest)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0291-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0291-183">Requirements</span></span>



| <span data-ttu-id="a0291-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0291-184">Requirement</span></span> | <span data-ttu-id="a0291-185">Valore</span><span class="sxs-lookup"><span data-stu-id="a0291-185">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0291-186">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0291-186">Minimum supported client</span></span><br/> | <span data-ttu-id="a0291-187">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a0291-187">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a0291-188">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0291-188">Minimum supported server</span></span><br/> | <span data-ttu-id="a0291-189">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0291-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a0291-190">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0291-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0291-191"><dt>SSPI. h (include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0291-191"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="a0291-192">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0291-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="a0291-193"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0291-193"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="a0291-194">DLL</span><span class="sxs-lookup"><span data-stu-id="a0291-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0291-195"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0291-195"><dt>Secur32.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="a0291-196">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0291-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0291-197">Funzioni SSPI</span><span class="sxs-lookup"><span data-stu-id="a0291-197">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="a0291-198">**AcceptSecurityContext (digest)**</span><span class="sxs-lookup"><span data-stu-id="a0291-198">**AcceptSecurityContext (Digest)**</span></span>](acceptsecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="a0291-199">**DecryptMessage (digest)**</span><span class="sxs-lookup"><span data-stu-id="a0291-199">**DecryptMessage (Digest)**</span></span>](decryptmessage--digest.md)
</dt> <dt>

[<span data-ttu-id="a0291-200">**InitializeSecurityContext (digest)**</span><span class="sxs-lookup"><span data-stu-id="a0291-200">**InitializeSecurityContext (Digest)**</span></span>](initializesecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="a0291-201">**QueryContextAttributes (digest)**</span><span class="sxs-lookup"><span data-stu-id="a0291-201">**QueryContextAttributes (Digest)**</span></span>](querycontextattributes--digest.md)
</dt> <dt>

[<span data-ttu-id="a0291-202">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="a0291-202">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[<span data-ttu-id="a0291-203">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="a0291-203">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
