---
description: Decrittografa un singolo pacchetto di protocollo SSL (Secure Sockets Layer).
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: Funzione SslDecryptPacket (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cd568596b7e780242c0ff8d9c522a9e1758c60b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967181"
---
# <a name="ssldecryptpacket-function"></a><span data-ttu-id="f2c75-103">SslDecryptPacket (funzione)</span><span class="sxs-lookup"><span data-stu-id="f2c75-103">SslDecryptPacket function</span></span>

<span data-ttu-id="f2c75-104">la funzione **SslDecryptPacket** decrittografa un singolo pacchetto di protocollo SSL ( [*Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="f2c75-104">the **SslDecryptPacket** function decrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c75-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2c75-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f2c75-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2c75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2c75-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2c75-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c75-108">Handle dell'istanza del provider del protocollo SSL.</span><span class="sxs-lookup"><span data-stu-id="f2c75-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="f2c75-109">*HKEY* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f2c75-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c75-110">Handle per la chiave utilizzata per decrittografare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f2c75-110">The handle to the key that is used to decrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="f2c75-111">*pbInput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2c75-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c75-112">Puntatore al buffer che contiene il pacchetto da decrittografare.</span><span class="sxs-lookup"><span data-stu-id="f2c75-112">A pointer to the buffer that contains the packet to be decrypted.</span></span>

</dd> <dt>

<span data-ttu-id="f2c75-113">*cbInput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2c75-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c75-114">Lunghezza, in byte, del buffer *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="f2c75-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f2c75-115">*pbOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f2c75-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c75-116">Puntatore a un buffer contenente il pacchetto decrittografato.</span><span class="sxs-lookup"><span data-stu-id="f2c75-116">A pointer to a buffer to contain the decrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="f2c75-117">*cbOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2c75-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c75-118">Lunghezza, byte, del buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="f2c75-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f2c75-119">*pcbResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f2c75-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c75-120">Numero di byte scritti nel buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="f2c75-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f2c75-121">*SequenceNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2c75-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c75-122">Numero di sequenza che corrisponde a questo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f2c75-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="f2c75-123">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2c75-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c75-124">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="f2c75-124">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2c75-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2c75-125">Return value</span></span>

<span data-ttu-id="f2c75-126">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="f2c75-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="f2c75-127">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f2c75-127">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="f2c75-128">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="f2c75-128">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="f2c75-129">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2c75-129">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="f2c75-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2c75-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="f2c75-131"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f2c75-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="f2c75-132">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="f2c75-132">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f2c75-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2c75-133">Remarks</span></span>

<span data-ttu-id="f2c75-134">La lunghezza del pacchetto può essere zero, ad esempio quando viene decrittografato un messaggio "HelloRequest".</span><span class="sxs-lookup"><span data-stu-id="f2c75-134">The length of the packet can be zero, such as when a "HelloRequest" message is decrypted.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2c75-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2c75-135">Requirements</span></span>



| <span data-ttu-id="f2c75-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2c75-136">Requirement</span></span> | <span data-ttu-id="f2c75-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f2c75-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c75-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2c75-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f2c75-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2c75-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f2c75-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2c75-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f2c75-141">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f2c75-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f2c75-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2c75-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2c75-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2c75-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="f2c75-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f2c75-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2c75-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2c75-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

