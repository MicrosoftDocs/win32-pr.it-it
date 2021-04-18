---
description: Consente di decrittografare un messaggio utilizzando NTLM.
ms.assetid: 44c63152-507d-4769-9c0c-d275d2b0deac
title: Funzione DecryptMessage (NTLM)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 707f1bcd9ae697de0c3e23529fe2857f58d0e5e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313745"
---
# <a name="decryptmessage-ntlm-function"></a><span data-ttu-id="bfa14-103">Funzione DecryptMessage (NTLM)</span><span class="sxs-lookup"><span data-stu-id="bfa14-103">DecryptMessage (NTLM) function</span></span>

<span data-ttu-id="bfa14-104">La funzione **DecryptMessage (NTLM)** decrittografa un messaggio.</span><span class="sxs-lookup"><span data-stu-id="bfa14-104">The **DecryptMessage (NTLM)** function decrypts a message.</span></span> <span data-ttu-id="bfa14-105">Alcuni pacchetti non crittografano e decrittografano i messaggi, bensì eseguono e controllano un [*hash*](../secgloss/h-gly.md)di integrità.</span><span class="sxs-lookup"><span data-stu-id="bfa14-105">Some packages do not encrypt and decrypt messages but rather perform and check an integrity [*hash*](../secgloss/h-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="bfa14-106">[**EncryptMessage (NTLM)**](encryptmessage--ntlm.md) e **DecryptMessage (NTLM)** possono essere chiamati contemporaneamente da due thread diversi in un contesto SSPI (Single [*Security Support Provider Interface*](../secgloss/s-gly.md) ) se è in esecuzione la crittografia di un thread e l'altro viene decrittografato.</span><span class="sxs-lookup"><span data-stu-id="bfa14-106">[**EncryptMessage (NTLM)**](encryptmessage--ntlm.md) and **DecryptMessage (NTLM)** can be called at the same time from two different threads in a single [*security support provider interface*](../secgloss/s-gly.md) (SSPI) context if one thread is encrypting and the other is decrypting.</span></span> <span data-ttu-id="bfa14-107">Se più di un thread sta per essere crittografato o più di un thread viene decrittografato, ogni thread deve ottenere un contesto univoco.</span><span class="sxs-lookup"><span data-stu-id="bfa14-107">If more than one thread is encrypting, or more than one thread is decrypting, each thread should obtain a unique context.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa14-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfa14-108">Syntax</span></span>

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a><span data-ttu-id="bfa14-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bfa14-109">Parameters</span></span>

<span data-ttu-id="bfa14-110">*phContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfa14-110">*phContext* \[in\]</span></span>

<span data-ttu-id="bfa14-111">Handle per il [*contesto di sicurezza*](../secgloss/s-gly.md) da utilizzare per decrittografare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="bfa14-111">A handle to the [*security context*](../secgloss/s-gly.md) to be used to decrypt the message.</span></span>

<span data-ttu-id="bfa14-112">*PMessage* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="bfa14-112">*pMessage* \[in, out\]</span></span>

<span data-ttu-id="bfa14-113">Puntatore a una struttura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="bfa14-113">A pointer to a [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="bfa14-114">In input la struttura fa riferimento a una o più strutture [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) .</span><span class="sxs-lookup"><span data-stu-id="bfa14-114">On input, the structure references one or more [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) structures.</span></span> <span data-ttu-id="bfa14-115">Almeno uno di questi deve essere di tipo SECBUFFER \_ Data.</span><span class="sxs-lookup"><span data-stu-id="bfa14-115">At least one of these must be of type SECBUFFER\_DATA.</span></span> <span data-ttu-id="bfa14-116">Il buffer contiene il messaggio crittografato.</span><span class="sxs-lookup"><span data-stu-id="bfa14-116">That buffer contains the encrypted message.</span></span> <span data-ttu-id="bfa14-117">Il messaggio crittografato viene decrittografato sul posto, sovrascrivendo il contenuto originale del buffer.</span><span class="sxs-lookup"><span data-stu-id="bfa14-117">The encrypted message is decrypted in place, overwriting the original contents of its buffer.</span></span>

<span data-ttu-id="bfa14-118">*MessageSeqNo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfa14-118">*MessageSeqNo* \[in\]</span></span>

<span data-ttu-id="bfa14-119">Numero di sequenza previsto dall'applicazione di trasporto, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="bfa14-119">The sequence number expected by the transport application, if any.</span></span> <span data-ttu-id="bfa14-120">Se l'applicazione di trasporto non mantiene i numeri di sequenza, questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="bfa14-120">If the transport application does not maintain sequence numbers, this parameter must be set to zero.</span></span>

<span data-ttu-id="bfa14-121">*pfQOP* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bfa14-121">*pfQOP* \[out\]</span></span>

<span data-ttu-id="bfa14-122">Puntatore a una variabile di tipo **ULONG** che riceve flag specifici del pacchetto che indicano la qualità della protezione.</span><span class="sxs-lookup"><span data-stu-id="bfa14-122">A pointer to a variable of type **ULONG** that receives package-specific flags that indicate the quality of protection.</span></span>

<span data-ttu-id="bfa14-123">Questo parametro può essere il seguente flag.</span><span class="sxs-lookup"><span data-stu-id="bfa14-123">This parameter can be the following flag.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="bfa14-124">Valore</span><span class="sxs-lookup"><span data-stu-id="bfa14-124">Value</span></span></th><th><span data-ttu-id="bfa14-125">Significato</span><span class="sxs-lookup"><span data-stu-id="bfa14-125">Meaning</span></span></th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <span data-ttu-id="bfa14-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="bfa14-126"><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </span></span></dl></td><td><span data-ttu-id="bfa14-127">Il messaggio non è stato crittografato, ma è stata generata un'intestazione o un trailer.</span><span class="sxs-lookup"><span data-stu-id="bfa14-127">The message was not encrypted, but a header or trailer was produced.</span></span><br/><blockquote>[!Note]<br />
<span data-ttu-id="bfa14-128">KERB_WRAP_NO_ENCRYPT ha lo stesso valore e lo stesso significato.</span><span class="sxs-lookup"><span data-stu-id="bfa14-128">KERB_WRAP_NO_ENCRYPT has the same value and the same meaning.</span></span></blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a><span data-ttu-id="bfa14-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bfa14-129">Return value</span></span>

<span data-ttu-id="bfa14-130">Se la funzione verifica che il messaggio sia stato ricevuto nella sequenza corretta, la funzione restituisce SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bfa14-130">If the function verifies that the message was received in the correct sequence, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="bfa14-131">Se la funzione non riesce a decrittografare il messaggio, restituisce uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="bfa14-131">If the function fails to decrypt the message, it returns one of the following error codes.</span></span>

| <span data-ttu-id="bfa14-132">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bfa14-132">Return code</span></span>                     | <span data-ttu-id="bfa14-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfa14-133">Description</span></span>                                                                                                                                                              |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa14-134">**SEC \_ E \_ messaggio incompleto \_**</span><span class="sxs-lookup"><span data-stu-id="bfa14-134">**SEC\_E\_INCOMPLETE\_MESSAGE**</span></span> | <span data-ttu-id="bfa14-135">I dati nel buffer di input sono incompleti.</span><span class="sxs-lookup"><span data-stu-id="bfa14-135">The data in the input buffer is incomplete.</span></span> <span data-ttu-id="bfa14-136">L'applicazione deve leggere più dati dal server e chiamare di nuovo [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="bfa14-136">The application needs to read more data from the server and call [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) again.</span></span> |
| <span data-ttu-id="bfa14-137">**SEC \_ E \_ fuori \_ \_ sequenza**</span><span class="sxs-lookup"><span data-stu-id="bfa14-137">**SEC\_E\_OUT\_OF\_SEQUENCE**</span></span>   | <span data-ttu-id="bfa14-138">Il messaggio non è stato ricevuto nella sequenza corretta.</span><span class="sxs-lookup"><span data-stu-id="bfa14-138">The message was not received in the correct sequence.</span></span>                                                                                                                    |

## <a name="remarks"></a><span data-ttu-id="bfa14-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="bfa14-139">Remarks</span></span>

<span data-ttu-id="bfa14-140">A volte un'applicazione legge i dati dalla parte remota, tenta di decrittografarla utilizzando **DecryptMessage (NTLM)** e rileva che **DecryptMessage (NTLM)** ha avuto esito positivo, ma i buffer di output sono vuoti.</span><span class="sxs-lookup"><span data-stu-id="bfa14-140">Sometimes an application will read data from the remote party, attempt to decrypt it by using **DecryptMessage (NTLM)**, and discover that **DecryptMessage (NTLM)** succeeded but the output buffers are empty.</span></span> <span data-ttu-id="bfa14-141">Si tratta di un comportamento normale che le applicazioni devono essere in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="bfa14-141">This is normal behavior, and applications must be able to deal with it.</span></span>

<span data-ttu-id="bfa14-142">**Windows XP:** Questa funzione è nota anche come **UnsealMessage**.</span><span class="sxs-lookup"><span data-stu-id="bfa14-142">**Windows XP:** This function was also known as **UnsealMessage**.</span></span> <span data-ttu-id="bfa14-143">Le applicazioni devono ora utilizzare solo **DecryptMessage (NTLM)** .</span><span class="sxs-lookup"><span data-stu-id="bfa14-143">Applications should now use **DecryptMessage (NTLM)** only.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfa14-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfa14-144">Requirements</span></span>

| <span data-ttu-id="bfa14-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfa14-145">Requirement</span></span> | <span data-ttu-id="bfa14-146">Valore</span><span class="sxs-lookup"><span data-stu-id="bfa14-146">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="bfa14-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfa14-147">Minimum supported client</span></span> | <span data-ttu-id="bfa14-148">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bfa14-148">Windows XP \[desktop apps only\]</span></span>          |
| <span data-ttu-id="bfa14-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfa14-149">Minimum supported server</span></span> | <span data-ttu-id="bfa14-150">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bfa14-150">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="bfa14-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bfa14-151">Header</span></span>                   | <span data-ttu-id="bfa14-152">SSPI. h (include Security. h)</span><span class="sxs-lookup"><span data-stu-id="bfa14-152">Sspi.h (include Security.h)</span></span>               |
| <span data-ttu-id="bfa14-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="bfa14-153">Library</span></span>                  | <span data-ttu-id="bfa14-154">Secur32. lib</span><span class="sxs-lookup"><span data-stu-id="bfa14-154">Secur32.lib</span></span>                               |
| <span data-ttu-id="bfa14-155">DLL</span><span class="sxs-lookup"><span data-stu-id="bfa14-155">DLL</span></span>                      | <span data-ttu-id="bfa14-156">Secur32.dll</span><span class="sxs-lookup"><span data-stu-id="bfa14-156">Secur32.dll</span></span>                               |

## <a name="see-also"></a><span data-ttu-id="bfa14-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bfa14-157">See also</span></span>

- [<span data-ttu-id="bfa14-158">Funzioni SSPI</span><span class="sxs-lookup"><span data-stu-id="bfa14-158">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
- [<span data-ttu-id="bfa14-159">**EncryptMessage (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="bfa14-159">**EncryptMessage (NTLM)**</span></span>](encryptmessage--ntlm.md)
- [<span data-ttu-id="bfa14-160">**SecBuffer**</span><span class="sxs-lookup"><span data-stu-id="bfa14-160">**SecBuffer**</span></span>](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [<span data-ttu-id="bfa14-161">**SecBufferDesc**</span><span class="sxs-lookup"><span data-stu-id="bfa14-161">**SecBufferDesc**</span></span>](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
