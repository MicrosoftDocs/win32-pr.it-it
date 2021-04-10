---
description: La funzione RKeyPFXInstall non è supportata.
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: Funzione RKeyPFXInstall (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyPFXInstall
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 4908b7224a02f5a28b876b1ff67cbcec7d23df5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966697"
---
# <a name="rkeypfxinstall-function"></a><span data-ttu-id="75b6e-103">RKeyPFXInstall (funzione)</span><span class="sxs-lookup"><span data-stu-id="75b6e-103">RKeyPFXInstall function</span></span>

<span data-ttu-id="75b6e-104">La funzione **RKeyPFXInstall** non è supportata.</span><span class="sxs-lookup"><span data-stu-id="75b6e-104">The **RKeyPFXInstall** function is not supported.</span></span>

<span data-ttu-id="75b6e-105">**Windows Server 2003:** La funzione **RKeyPFXInstall** installa un certificato in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="75b6e-105">**Windows Server 2003:** The **RKeyPFXInstall** function installs a certificate on a remote computer.</span></span> <span data-ttu-id="75b6e-106">Si noti che questo comportamento è stato modificato con Windows Server 2003 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="75b6e-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="75b6e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75b6e-107">Syntax</span></span>


```C++
ULONG RKeyPFXInstall(
  _In_ KEYSVCC_HANDLE         hKeySvcCli,
  _In_ PKEYSVC_BLOB           pPFX,
  _In_ PKEYSVC_UNICODE_STRING pPassword,
  _In_ ULONG                  ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="75b6e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="75b6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b6e-109">*hKeySvcCli* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75b6e-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b6e-110">Handle [**di \_ handle KEYSVCC**](keysvcc-handle.md) precedentemente aperto da [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span><span class="sxs-lookup"><span data-stu-id="75b6e-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="75b6e-111">L'handle rappresenta il computer remoto che riceverà il certificato.</span><span class="sxs-lookup"><span data-stu-id="75b6e-111">The handle represents the remote computer that will receive the certificate.</span></span> <span data-ttu-id="75b6e-112">Questo valore non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="75b6e-112">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="75b6e-113">*pPFX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75b6e-113">*pPFX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b6e-114">Puntatore a una struttura [**\_ BLOB KEYSVC**](keysvc-blob.md) che rappresenta il certificato da installare.</span><span class="sxs-lookup"><span data-stu-id="75b6e-114">A pointer to a [**KEYSVC\_BLOB**](keysvc-blob.md) structure that represents the certificate to install.</span></span> <span data-ttu-id="75b6e-115">Il BLOB è in formato [*PKCS \# 12*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="75b6e-115">The BLOB is in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> <dt>

<span data-ttu-id="75b6e-116">*ppassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75b6e-116">*pPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b6e-117">Puntatore a una struttura [**di \_ \_ stringhe Unicode KEYSVC**](keysvc-unicode-string.md) che rappresenta la password per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="75b6e-117">A pointer to a [**KEYSVC\_UNICODE\_STRING**](keysvc-unicode-string.md) structure that represents the password for the BLOB.</span></span> <span data-ttu-id="75b6e-118">Al termine dell'utilizzo della password, cancellare la password dalla memoria chiamando la funzione [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="75b6e-118">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="75b6e-119">Per ulteriori informazioni sulla protezione delle password, vedere [gestione delle password](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="75b6e-119">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="75b6e-120">*ulFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75b6e-120">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b6e-121">Flag che specificano le opzioni di installazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="75b6e-121">Flags that specify the certificate installation options.</span></span> <span data-ttu-id="75b6e-122">Questo parametro può essere uno zero o una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="75b6e-122">This parameter can be a zero or a combination of the following values.</span></span>



| <span data-ttu-id="75b6e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="75b6e-123">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="75b6e-124">Significato</span><span class="sxs-lookup"><span data-stu-id="75b6e-124">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <span data-ttu-id="75b6e-125"><dt>**Crypt \_ Esportabile**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="75b6e-125"><dt>**CRYPT\_EXPORTABLE**</dt> <dt></dt></span></span> </dl>              | <span data-ttu-id="75b6e-126">Le chiavi importate sono contrassegnate come esportabili.</span><span class="sxs-lookup"><span data-stu-id="75b6e-126">Imported keys are marked as exportable.</span></span><br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <span data-ttu-id="75b6e-127"><dt>**Crypt \_ \_keyset del computer**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="75b6e-127"><dt>**CRYPT\_MACHINE\_KEYSET**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="75b6e-128">Le chiavi private vengono archiviate nel computer remoto e non nell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="75b6e-128">Private keys are stored under the remote computer and not under the current user.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b6e-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75b6e-129">Return value</span></span>

<span data-ttu-id="75b6e-130">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="75b6e-130">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="75b6e-131">Se la funzione ha esito negativo, il valore restituito è un **ULONG** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="75b6e-131">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b6e-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75b6e-132">Requirements</span></span>



| <span data-ttu-id="75b6e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="75b6e-133">Requirement</span></span> | <span data-ttu-id="75b6e-134">Valore</span><span class="sxs-lookup"><span data-stu-id="75b6e-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75b6e-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75b6e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="75b6e-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="75b6e-136">None supported</span></span><br/>                                                             |
| <span data-ttu-id="75b6e-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75b6e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="75b6e-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="75b6e-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75b6e-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75b6e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="75b6e-140"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="75b6e-140"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75b6e-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75b6e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b6e-142">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="75b6e-142">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="75b6e-143">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="75b6e-143">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 
