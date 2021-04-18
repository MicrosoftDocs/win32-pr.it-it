---
description: Consente di decrittografare un messaggio tramite Negotiate.
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: Funzione DecryptMessage (Negotiate)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: b4c8af2c79145950f9f42b52a662aba8ac13064f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308152"
---
# <a name="decryptmessage-negotiate-function"></a><span data-ttu-id="a102d-103">Funzione DecryptMessage (Negotiate)</span><span class="sxs-lookup"><span data-stu-id="a102d-103">DecryptMessage (Negotiate) function</span></span>

<span data-ttu-id="a102d-104">La funzione **DecryptMessage (Negotiate)** decrittografa un messaggio.</span><span class="sxs-lookup"><span data-stu-id="a102d-104">The **DecryptMessage (Negotiate)** function decrypts a message.</span></span> <span data-ttu-id="a102d-105">Alcuni pacchetti non crittografano e decrittografano i messaggi, bensì eseguono e controllano un [*hash*](../secgloss/h-gly.md)di integrità.</span><span class="sxs-lookup"><span data-stu-id="a102d-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="a102d-106">[**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) e **DecryptMessage (Negotiate)** possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se un thread esegue la crittografia e l'altro esegue la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="a102d-106">[**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) and **DecryptMessage (Negotiate)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="a102d-107">Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.</span><span class="sxs-lookup"><span data-stu-id="a102d-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="a102d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a102d-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="a102d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a102d-109">Parameters</span></span>

<span data-ttu-id="a102d-110">*phContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a102d-110">*phContext* \[in\]</span></span>

<span data-ttu-id="a102d-111">Handle per il [*contesto di sicurezza*](../secgloss/s-gly.md) da utilizzare per decrittografare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="a102d-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="a102d-112">*PMessage* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a102d-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="a102d-113">Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="a102d-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="a102d-114">In input la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) .</span><span class="sxs-lookup"><span data-stu-id="a102d-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures .</span></span> <span data-ttu-id="a102d-115">Almeno uno di questi deve essere di tipo SECBUFFER \_ Data.</span><span class="sxs-lookup"><span data-stu-id="a102d-115">At least one of these must be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="a102d-116">Il buffer contiene il messaggio crittografato.</span><span class="sxs-lookup"><span data-stu-id="a102d-116">That buffer contains the encrypted message.</span></span> <span data-ttu-id="a102d-117">Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.</span><span class="sxs-lookup"><span data-stu-id="a102d-117">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="a102d-118">*MessageSeqNo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a102d-118">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="a102d-119">Numero di sequenza previsto dall'applicazione di trasporto, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="a102d-119">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="a102d-120">Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="a102d-120">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="a102d-121">*pfQOP* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a102d-121">*pfQOP* \[out\]</span></span>

<span data-ttu-id="a102d-122">Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.</span><span class="sxs-lookup"><span data-stu-id="a102d-122">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="a102d-123">Questo parametro può essere il seguente flag.</span><span class="sxs-lookup"><span data-stu-id="a102d-123">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="a102d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a102d-124">Value</span></span></th><th><span data-ttu-id="a102d-125">Significato</span><span class="sxs-lookup"><span data-stu-id="a102d-125">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="a102d-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a102d-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="a102d-127">Il messaggio non è stato crittografato, ma è stata generata un'intestazione o un trailer.</span><span class="sxs-lookup"><span data-stu-id="a102d-127">The message was not encrypted, but a header or trailer was produced.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="a102d-128">KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</span><span class="sxs-lookup"><span data-stu-id="a102d-128">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a><span data-ttu-id="a102d-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a102d-129">Return value</span></span>

<span data-ttu-id="a102d-130">Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a102d-130">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="a102d-131">Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="a102d-131">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="a102d-132">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a102d-132">Return code</span></span>                     | <span data-ttu-id="a102d-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a102d-133">Description</span></span>                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a102d-134">**SEC \_ E \_ messaggio incompleto \_**</span><span class="sxs-lookup"><span data-stu-id="a102d-134">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="a102d-135">I dati nel buffer di input sono incompleti.</span><span class="sxs-lookup"><span data-stu-id="a102d-135">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="a102d-136">L'applicazione deve leggere più dati dal server e chiamare di nuovo [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="a102d-136">The application needs to read more data from the server and call [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) again.</span></span> |
| <span data-ttu-id="a102d-137">**SEC \_ E \_ fuori \_ \_ sequenza**</span><span class="sxs-lookup"><span data-stu-id="a102d-137">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="a102d-138">Il messaggio non è stato ricevuto nella sequenza corretta.</span><span class="sxs-lookup"><span data-stu-id="a102d-138">The message was not received in the correct sequence.</span></span>                                                                                                                              |

## <a name="remarks"></a><span data-ttu-id="a102d-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="a102d-139">Remarks</span></span>

<span data-ttu-id="a102d-140">In alcuni casi un'applicazione legge i dati dalla parte remota, tenta di decrittografarli usando **DecryptMessage (Negotiate)** e rileva che **DecryptMessage (Negotiate)** ha avuto esito positivo, ma i buffer di output sono vuoti.</span><span class="sxs-lookup"><span data-stu-id="a102d-140">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (Negotiate)**, and discover that **DecryptMessage (Negotiate)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="a102d-141">Si tratta di un comportamento normale che le applicazioni devono essere in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="a102d-141">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="a102d-142">**Windows XP:** Questa funzione è nota anche come **UnsealMessage**.</span><span class="sxs-lookup"><span data-stu-id="a102d-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="a102d-143">Le applicazioni devono ora usare solo **DecryptMessage (Negotiate)** .</span><span class="sxs-lookup"><span data-stu-id="a102d-143">Applications should now use **DecryptMessage (Negotiate)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="a102d-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a102d-144">Requirements</span></span>

| <span data-ttu-id="a102d-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="a102d-145">Requirement</span></span> | <span data-ttu-id="a102d-146">Valore</span><span class="sxs-lookup"><span data-stu-id="a102d-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a102d-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a102d-147">Minimum supported client</span></span> | <span data-ttu-id="a102d-148">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a102d-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="a102d-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a102d-149">Minimum supported server</span></span> | <span data-ttu-id="a102d-150">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a102d-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="a102d-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a102d-151">Header</span></span>                   | <span data-ttu-id="a102d-152">SSPI. h (include Security. h)</span><span class="sxs-lookup"><span data-stu-id="a102d-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="a102d-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="a102d-153">Library</span></span>                  | <span data-ttu-id="a102d-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="a102d-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="a102d-155">DLL</span><span class="sxs-lookup"><span data-stu-id="a102d-155">DLL</span></span>                      | <span data-ttu-id="a102d-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="a102d-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="a102d-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a102d-157">See also</span></span>

- [<span data-ttu-id="a102d-158">Funzioni SSPI</span><span class="sxs-lookup"><span data-stu-id="a102d-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="a102d-159">**EncryptMessage (negoziazione)**</span><span class="sxs-lookup"><span data-stu-id="a102d-159">**EncryptMessage (Negotiate)**</span></span>](encryptmessage--negotiate.md)
- [<span data-ttu-id="a102d-160">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="a102d-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="a102d-161">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="a102d-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
