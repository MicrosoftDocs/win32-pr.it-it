---
description: Crea una chiave temporanea da usare durante l'autenticazione che si verifica durante l'handshake SSL (Secure Sockets Layer Protocol).
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: Funzione SslCreateEphemeralKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateEphemeralKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452b0166da367bb6b1530f5669e55b7ca909e13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310763"
---
# <a name="sslcreateephemeralkey-function"></a><span data-ttu-id="070a8-103">SslCreateEphemeralKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="070a8-103">SslCreateEphemeralKey function</span></span>

<span data-ttu-id="070a8-104">La funzione **SslCreateEphemeralKey** crea una chiave temporanea da usare durante l'autenticazione che si verifica durante l'handshake SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="070a8-104">The **SslCreateEphemeralKey** function creates an ephemeral key for use during the authentication that occurs during the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span>

## <a name="syntax"></a><span data-ttu-id="070a8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="070a8-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateEphemeralKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phEphemeralKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _In_  DWORD              dwKeyBitLen,
  _In_  PBYTE              pbParams,
  _In_  DWORD              cbParams,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="070a8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="070a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="070a8-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="070a8-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="070a8-108">Handle dell'istanza del provider del protocollo SSL.</span><span class="sxs-lookup"><span data-stu-id="070a8-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="070a8-109">*phEphemeralKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="070a8-109">*phEphemeralKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="070a8-110">Handle della chiave temporanea.</span><span class="sxs-lookup"><span data-stu-id="070a8-110">The handle of the ephemeral key.</span></span>

</dd> <dt>

<span data-ttu-id="070a8-111">*dwProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="070a8-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="070a8-112">Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="070a8-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="070a8-113">*dwCipherSuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="070a8-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="070a8-114">Uno dei valori dell' [**identificatore del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="070a8-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="070a8-115">*dwKeyType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="070a8-115">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="070a8-116">Uno dei valori dell' [**identificatore del tipo di chiave del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="070a8-116">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="070a8-117">Impostare questo parametro su zero per i tipi di chiave che non sono la [*crittografia a curva ellittica*](/windows/desktop/SecGloss/e-gly) (ecc).</span><span class="sxs-lookup"><span data-stu-id="070a8-117">Set this parameter to zero for key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC).</span></span>

</dd> <dt>

<span data-ttu-id="070a8-118">*dwKeyBitLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="070a8-118">*dwKeyBitLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="070a8-119">Lunghezza, espressa in bit, della chiave.</span><span class="sxs-lookup"><span data-stu-id="070a8-119">The length, in bits, of the key.</span></span>

</dd> <dt>

<span data-ttu-id="070a8-120">*pbParams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="070a8-120">*pbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="070a8-121">Puntatore a un buffer che contiene i parametri per la chiave che deve essere creata.</span><span class="sxs-lookup"><span data-stu-id="070a8-121">A pointer to a buffer to contain parameters for the key that is to be created.</span></span> <span data-ttu-id="070a8-122">Se non si usa un pacchetto di crittografia dhe ( [*Diffie-Hellman (effimero)*](/windows/desktop/SecGloss/d-gly) , impostare il parametro *pbParams* su **null** e il parametro *cbParams* su zero.</span><span class="sxs-lookup"><span data-stu-id="070a8-122">If a [*Diffie-Hellman (ephemeral) key-exchange algorithm*](/windows/desktop/SecGloss/d-gly) (DHE) cipher suite is not used, set the *pbParams* parameter to **NULL** and the *cbParams* parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="070a8-123">*cbParams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="070a8-123">*cbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="070a8-124">Lunghezza, in byte, dei dati nel buffer di *pbParams* .</span><span class="sxs-lookup"><span data-stu-id="070a8-124">The length, in bytes, of the data in the *pbParams* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="070a8-125">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="070a8-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="070a8-126">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="070a8-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="070a8-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="070a8-127">Return value</span></span>

<span data-ttu-id="070a8-128">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="070a8-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="070a8-129">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="070a8-129">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="070a8-130">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="070a8-130">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="070a8-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="070a8-131">Description</span></span>                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="070a8-132"><dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria</span><span class="sxs-lookup"><span data-stu-id="070a8-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="070a8-133">La memoria disponibile non è sufficiente per allocare il buffer.</span><span class="sxs-lookup"><span data-stu-id="070a8-133">There is insufficient memory to allocate the buffer.</span></span><br/> |
| <dl> <span data-ttu-id="070a8-134"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="070a8-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="070a8-135">Handle *hSslProvider* non valido.</span><span class="sxs-lookup"><span data-stu-id="070a8-135">The *hSslProvider* handle is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="070a8-136"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="070a8-136"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="070a8-137">Uno dei parametri specificati non è valido.</span><span class="sxs-lookup"><span data-stu-id="070a8-137">One of the supplied parameters is not valid.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="070a8-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="070a8-138">Remarks</span></span>

<span data-ttu-id="070a8-139">Quando si usa un pacchetto di crittografia DHE, l'implementazione SSL interna passa i parametri *p* e *g* del server alla funzione **SslCreateEphemeralKey** nei parametri *pbParams* e *cbParams* .</span><span class="sxs-lookup"><span data-stu-id="070a8-139">When using a DHE cipher suite, the internal SSL implementation passes server *p* and *g* parameters to the **SslCreateEphemeralKey** function in the *pbParams* and *cbParams* parameters.</span></span>

<span data-ttu-id="070a8-140">Il formato dei dati nel buffer *pbParams* è identico a quello usato quando si imposta la proprietà [**BCRYPT \_ DH \_ Parameters**](cng-property-identifiers.md) e inizia con una struttura di [**intestazione di \_ \_ parametro BCRYPT \_ DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="070a8-140">The format of the data in the *pbParams* buffer is the same as that used when setting the [**BCRYPT\_DH\_PARAMETERS**](cng-property-identifiers.md) property, and it starts with a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="070a8-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="070a8-141">Requirements</span></span>



| <span data-ttu-id="070a8-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="070a8-142">Requirement</span></span> | <span data-ttu-id="070a8-143">Valore</span><span class="sxs-lookup"><span data-stu-id="070a8-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="070a8-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="070a8-144">Minimum supported client</span></span><br/> | <span data-ttu-id="070a8-145">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="070a8-145">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="070a8-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="070a8-146">Minimum supported server</span></span><br/> | <span data-ttu-id="070a8-147">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="070a8-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="070a8-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="070a8-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="070a8-149"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="070a8-149"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="070a8-150">DLL</span><span class="sxs-lookup"><span data-stu-id="070a8-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="070a8-151"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="070a8-151"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

