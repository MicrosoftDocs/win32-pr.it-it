---
description: Crittografa un singolo pacchetto SSL (Secure Sockets Layer Protocol).
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: Funzione SslEncryptPacket (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEncryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e839b37e839fd09d5df5f9902474b7ce7c4c74a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319386"
---
# <a name="sslencryptpacket-function"></a><span data-ttu-id="a491c-103">SslEncryptPacket (funzione)</span><span class="sxs-lookup"><span data-stu-id="a491c-103">SslEncryptPacket function</span></span>

<span data-ttu-id="a491c-104">La funzione **SslEncryptPacket** crittografa un singolo pacchetto SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="a491c-104">The **SslEncryptPacket** function encrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="a491c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a491c-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEncryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwContentType,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a491c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a491c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a491c-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a491c-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a491c-108">Handle dell'istanza del provider del protocollo SSL.</span><span class="sxs-lookup"><span data-stu-id="a491c-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="a491c-109">*HKEY* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a491c-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a491c-110">Handle per la chiave utilizzata per crittografare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a491c-110">The handle to the key that is used to encrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="a491c-111">*pbInput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a491c-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a491c-112">Puntatore al buffer che contiene il pacchetto da crittografare.</span><span class="sxs-lookup"><span data-stu-id="a491c-112">A pointer to the buffer that contains the packet to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="a491c-113">*cbInput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a491c-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a491c-114">Lunghezza, in byte, del buffer *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="a491c-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a491c-115">*pbOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a491c-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a491c-116">Puntatore a un buffer per ricevere il pacchetto crittografato.</span><span class="sxs-lookup"><span data-stu-id="a491c-116">A pointer to a buffer to receive the encrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="a491c-117">*cbOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a491c-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a491c-118">Lunghezza, byte, del buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="a491c-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a491c-119">*pcbResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a491c-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a491c-120">Numero di byte scritti nel buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="a491c-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a491c-121">*SequenceNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a491c-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a491c-122">Numero di sequenza che corrisponde a questo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a491c-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="a491c-123">*dwContentType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a491c-123">*dwContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a491c-124">Tipo di contenuto che corrisponde a questo pacchetto, che specifica il protocollo di livello superiore usato per elaborare il pacchetto incluso.</span><span class="sxs-lookup"><span data-stu-id="a491c-124">The content type that corresponds to this packet, which specifies the higher level protocol used to process the enclosed packet.</span></span>



| <span data-ttu-id="a491c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a491c-125">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="a491c-126">Significato</span><span class="sxs-lookup"><span data-stu-id="a491c-126">Meaning</span></span>                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <span data-ttu-id="a491c-127"><dt>**CT \_ MODIFICARE \_ la \_ specifica di crittografia**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="a491c-127"><dt>**CT\_CHANGE\_CIPHER\_SPEC**</dt> <dt>20</dt></span></span> </dl> | <span data-ttu-id="a491c-128">Indica una modifica della strategia di crittografia.</span><span class="sxs-lookup"><span data-stu-id="a491c-128">Indicates a change in the ciphering strategy.</span></span><br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <span data-ttu-id="a491c-129"><dt>**CT \_ AVVISO**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="a491c-129"><dt>**CT\_ALERT**</dt> <dt>21</dt></span></span> </dl>                                          | <span data-ttu-id="a491c-130">Indica che il pacchetto racchiuso contiene un avviso.</span><span class="sxs-lookup"><span data-stu-id="a491c-130">Indicates that the enclosed packet contains an alert.</span></span><br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <span data-ttu-id="a491c-131"><dt>**CT \_ HANDSHAKe**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="a491c-131"><dt>**CT\_HANDSHAKE**</dt> <dt>22</dt></span></span> </dl>                              | <span data-ttu-id="a491c-132">Indica che il pacchetto racchiuso fa parte del protocollo di handshake.</span><span class="sxs-lookup"><span data-stu-id="a491c-132">Indicates that the enclosed packet is part of the handshake protocol.</span></span><br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <span data-ttu-id="a491c-133"><dt>**CT \_ APPLICATIONDATA**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="a491c-133"><dt>**CT\_APPLICATIONDATA**</dt> <dt>23</dt></span></span> </dl>            | <span data-ttu-id="a491c-134">Indica che il pacchetto contiene i dati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a491c-134">Indicates that the packet contains application data.</span></span><br/>                  |



 

</dd> <dt>

<span data-ttu-id="a491c-135">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a491c-135">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a491c-136">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="a491c-136">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a491c-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a491c-137">Return value</span></span>

<span data-ttu-id="a491c-138">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="a491c-138">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="a491c-139">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a491c-139">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="a491c-140">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="a491c-140">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="a491c-141">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="a491c-141">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="a491c-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a491c-142">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="a491c-143"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a491c-143"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="a491c-144">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="a491c-144">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a491c-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a491c-145">Requirements</span></span>



| <span data-ttu-id="a491c-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="a491c-146">Requirement</span></span> | <span data-ttu-id="a491c-147">Valore</span><span class="sxs-lookup"><span data-stu-id="a491c-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a491c-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a491c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a491c-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a491c-149">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a491c-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a491c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a491c-151">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a491c-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a491c-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a491c-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="a491c-153"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="a491c-153"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="a491c-154">DLL</span><span class="sxs-lookup"><span data-stu-id="a491c-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a491c-155"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a491c-155"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

