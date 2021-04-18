---
description: Contiene informazioni su un provider del servizio di crittografia (CSP) per smart card.
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: Struttura KERB_SMARTCARD_CSP_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KERB_SMARTCARD_CSP_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 03b1a8084e291dde5a4f1f2017e4e97f57640bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313295"
---
# <a name="kerb_smartcard_csp_info-structure"></a><span data-ttu-id="bf6fd-103">\_Struttura delle \_ informazioni CSP per la smart card \_</span><span class="sxs-lookup"><span data-stu-id="bf6fd-103">KERB\_SMARTCARD\_CSP\_INFO structure</span></span>

<span data-ttu-id="bf6fd-104">La struttura di **\_ \_ \_ informazioni CSP** per la smart card di bordo contiene informazioni su un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) per smart card.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-104">The **KERB\_SMARTCARD\_CSP\_INFO** structure contains information about a smart card [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="bf6fd-105">Questa struttura non è dichiarata in un'intestazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-105">This structure is not declared in a public header.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf6fd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf6fd-106">Syntax</span></span>


```C++
typedef struct _KERB_SMARTCARD_CSP_INFO {
  DWORD dwCspInfoLen;
  DWORD MessageType;
  union {
    PVOID   ContextInformation;
    ULONG64 SpaceHolderForWow64;
  };
  DWORD flags;
  DWORD KeySpec;
  ULONG nCardNameOffset;
  ULONG nReaderNameOffset;
  ULONG nContainerNameOffset;
  ULONG nCSPNameOffset;
  TCHAR bBuffer;
} KERB_SMARTCARD_CSP_INFO, *PKERB_SMARTCARD_CSP_INFO;
```



## <a name="members"></a><span data-ttu-id="bf6fd-107">Members</span><span class="sxs-lookup"><span data-stu-id="bf6fd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bf6fd-108">**dwCspInfoLen**</span><span class="sxs-lookup"><span data-stu-id="bf6fd-108">**dwCspInfoLen**</span></span>
</dt> <dd>

<span data-ttu-id="bf6fd-109">Dimensione, in byte, della struttura, inclusi i dati accodati.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-109">The size, in bytes, of this structure, including any appended data.</span></span>

</dd> <dt>

<span data-ttu-id="bf6fd-110">**MessageType**</span><span class="sxs-lookup"><span data-stu-id="bf6fd-110">**MessageType**</span></span>
</dt> <dd>

<span data-ttu-id="bf6fd-111">Tipo di messaggio passato.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-111">The type of message being passed.</span></span> <span data-ttu-id="bf6fd-112">Questo membro deve essere impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-112">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="bf6fd-113">**ContextInformation**</span><span class="sxs-lookup"><span data-stu-id="bf6fd-113">**ContextInformation**</span></span>
</dt> <dd>

<span data-ttu-id="bf6fd-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bf6fd-115">**SpaceHolderForWow64**</span><span class="sxs-lookup"><span data-stu-id="bf6fd-115">**SpaceHolderForWow64**</span></span>
</dt> <dd>

<span data-ttu-id="bf6fd-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bf6fd-117">**flags**</span><span class="sxs-lookup"><span data-stu-id="bf6fd-117">**flags**</span></span>
</dt> <dd>

<span data-ttu-id="bf6fd-118">Riservato.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bf6fd-119">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="bf6fd-119">**KeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="bf6fd-120">Chiave privata da usare dal contenitore di chiavi specificato all'interno del buffer **bBuffer**.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-120">The private key to use from the key container specified within the buffer **bBuffer**.</span></span> <span data-ttu-id="bf6fd-121">La chiave può essere uno dei valori seguenti, definiti in WinCrypt. h.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-121">The key can be one of the following values, defined in WinCrypt.h.</span></span>



| <span data-ttu-id="bf6fd-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bf6fd-122">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="bf6fd-123">Significato</span><span class="sxs-lookup"><span data-stu-id="bf6fd-123">Meaning</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="bf6fd-124"><dt>**Al \_ SCAMBIO**</dt> di stato <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bf6fd-124"><dt>**AT\_KEYEXCHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="bf6fd-125">La chiave è una chiave di scambio chiave.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-125">The key is a key-exchange key.</span></span><br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="bf6fd-126"><dt>**Al \_ FIRMA**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bf6fd-126"><dt>**AT\_SIGNATURE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="bf6fd-127">La chiave è una chiave di firma.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-127">The key is a signature key.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="bf6fd-128">**nCardNameOffset**</span><span class="sxs-lookup"><span data-stu-id="bf6fd-128">**nCardNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="bf6fd-129">Il numero di caratteri nel buffer **bBuffer** che precede il nome della smart card nel buffer.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-129">The number of characters in the **bBuffer** buffer that precede the name of the smart card in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf6fd-130">Se non viene specificato il nome della smart card, il buffer deve contenere una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-130">If the name of the smart card is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="bf6fd-131">**nReaderNameOffset**</span><span class="sxs-lookup"><span data-stu-id="bf6fd-131">**nReaderNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="bf6fd-132">Il numero di caratteri nel buffer **bBuffer** che precede il nome del lettore di smart card nel buffer.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-132">The number of characters in the **bBuffer** buffer that precede the name of the smart card reader in that buffer.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf6fd-133">Se non viene specificato il nome del lettore di smart card, il buffer deve contenere una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-133">If the name of the smart card reader is not provided, the buffer must contain an empty string.</span></span>

 

</dd> <dt>

<span data-ttu-id="bf6fd-134">**nContainerNameOffset**</span><span class="sxs-lookup"><span data-stu-id="bf6fd-134">**nContainerNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="bf6fd-135">Il numero di caratteri nel buffer **bBuffer** che precede il nome del contenitore di chiavi nel buffer.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-135">The number of characters in the **bBuffer** buffer that precede the name of the key container in that buffer.</span></span> <span data-ttu-id="bf6fd-136">Questa stringa non può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-136">This string cannot be empty.</span></span>

</dd> <dt>

<span data-ttu-id="bf6fd-137">**nCSPNameOffset**</span><span class="sxs-lookup"><span data-stu-id="bf6fd-137">**nCSPNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="bf6fd-138">Il numero di caratteri nel buffer **bBuffer** che precede il nome del CSP nel buffer.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-138">The number of characters in the **bBuffer** buffer that precede the name of the CSP in that buffer.</span></span>

</dd> <dt>

<span data-ttu-id="bf6fd-139">**bBuffer**</span><span class="sxs-lookup"><span data-stu-id="bf6fd-139">**bBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="bf6fd-140">Matrice di caratteri inizializzata su una lunghezza di `sizeof(DWORD)` .</span><span class="sxs-lookup"><span data-stu-id="bf6fd-140">An array of characters initialized to a length of `sizeof(DWORD)`.</span></span> <span data-ttu-id="bf6fd-141">Questo buffer contiene i nomi a cui fanno riferimento i membri **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset** e **nCSPNameOffset** , nonché tutti i dati aggiuntivi forniti dal CSP.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-141">This buffer contains the names referred to by the **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset**, and **nCSPNameOffset** members, as well as any additional data provided by the CSP.</span></span>

<span data-ttu-id="bf6fd-142">Tutti i nomi non specificati devono essere rappresentati in questo buffer da stringhe vuote.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-142">Any names that are not provided must be represented in this buffer by empty strings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf6fd-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf6fd-143">Remarks</span></span>

<span data-ttu-id="bf6fd-144">Quando questa struttura viene serializzata, i membri della struttura devono essere allineati ai limiti che sono multipli di 2 byte.</span><span class="sxs-lookup"><span data-stu-id="bf6fd-144">When this structure is serialized, the structure members must be aligned to boundaries that are multiples of 2 bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf6fd-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf6fd-145">Requirements</span></span>



| <span data-ttu-id="bf6fd-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf6fd-146">Requirement</span></span> | <span data-ttu-id="bf6fd-147">Valore</span><span class="sxs-lookup"><span data-stu-id="bf6fd-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bf6fd-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf6fd-148">Minimum supported client</span></span><br/> | <span data-ttu-id="bf6fd-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf6fd-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bf6fd-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf6fd-150">Minimum supported server</span></span><br/> | <span data-ttu-id="bf6fd-151">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf6fd-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf6fd-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf6fd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf6fd-153">**\_accesso al certificato da marciapiede \_**</span><span class="sxs-lookup"><span data-stu-id="bf6fd-153">**KERB\_CERTIFICATE\_LOGON**</span></span>](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
