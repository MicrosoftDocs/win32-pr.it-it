---
description: Imposta il valore del segreto utilizzato per derivare la chiave della sessione crittografica utilizzata per crittografare e decrittografare i dati.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: EncryptedData. sesecret, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c8d30355b022a593ca17519e3ccfa876a5b07b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324897"
---
# <a name="encrypteddatasetsecret-method"></a><span data-ttu-id="7d628-103">EncryptedData. sesecret, metodo</span><span class="sxs-lookup"><span data-stu-id="7d628-103">EncryptedData.SetSecret method</span></span>

<span data-ttu-id="7d628-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7d628-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7d628-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per crittografare e decrittografare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="7d628-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="7d628-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="7d628-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="7d628-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="7d628-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="7d628-108">Il metodo **sesecret** imposta il valore del segreto usato per derivare la chiave della [*sessione*](../secgloss/s-gly.md) crittografica usata per crittografare e decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="7d628-108">The **SetSecret** method sets the value of the secret used to derive the cryptographic [*session key*](../secgloss/s-gly.md) used to encrypt and decrypt data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d628-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d628-109">Syntax</span></span>


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7d628-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d628-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d628-111">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d628-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d628-112">Stringa che contiene un segreto utilizzato per creare una chiave crittografica della sessione.</span><span class="sxs-lookup"><span data-stu-id="7d628-112">A string that contains a secret used to create a session cryptographic key.</span></span>

</dd> <dt>

<span data-ttu-id="7d628-113">*SecretType* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7d628-113">*SecretType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7d628-114">Valore dell'enumerazione del [**\_ \_ tipo di segreto CAPICOM**](capicom-secret-type.md) che indica il tipo di segreto usato per generare la chiave della sessione.</span><span class="sxs-lookup"><span data-stu-id="7d628-114">A value of the [**CAPICOM\_SECRET\_TYPE**](capicom-secret-type.md) enumeration that indicates the kind of secret used to generate the session key.</span></span> <span data-ttu-id="7d628-115">Il valore predefinito è CAPICOM \_ Secret \_ password.</span><span class="sxs-lookup"><span data-stu-id="7d628-115">The default value is CAPICOM\_SECRET\_PASSWORD.</span></span> <span data-ttu-id="7d628-116">Questo parametro può essere il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="7d628-116">This parameter can be the following value.</span></span>



| <span data-ttu-id="7d628-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7d628-117">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="7d628-118">Significato</span><span class="sxs-lookup"><span data-stu-id="7d628-118">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <span data-ttu-id="7d628-119"><dt>**PASSWORD del segreto di CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d628-119"><dt>**CAPICOM\_SECRET\_PASSWORD**</dt></span></span> </dl> | <span data-ttu-id="7d628-120">La chiave di crittografia deve essere derivata da una password.</span><span class="sxs-lookup"><span data-stu-id="7d628-120">The encryption key is to be derived from a password.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d628-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d628-121">Return value</span></span>

<span data-ttu-id="7d628-122">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7d628-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d628-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d628-123">Remarks</span></span>

<span data-ttu-id="7d628-124">Il segreto viene usato per creare la chiave di sessione per la crittografia o la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="7d628-124">The secret is used to create the session key for encryption or decryption.</span></span> <span data-ttu-id="7d628-125">Per entrambe le operazioni è necessario usare lo stesso segreto.</span><span class="sxs-lookup"><span data-stu-id="7d628-125">The same secret must be used for both operations.</span></span> <span data-ttu-id="7d628-126">Se il segreto utilizzato per crittografare i dati viene perso, non sarà possibile decrittografare i dati crittografati.</span><span class="sxs-lookup"><span data-stu-id="7d628-126">If the secret used to encrypt data is lost, the encrypted data cannot be decrypted.</span></span>

<span data-ttu-id="7d628-127">Se appropriato per l'applicazione, prendere in considerazione l'uso di [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) o [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) per proteggere il segreto prima e dopo l'uso.</span><span class="sxs-lookup"><span data-stu-id="7d628-127">If appropriate for your application, consider using [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) or [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) to protect the secret before and after use.</span></span> <span data-ttu-id="7d628-128">Al termine, cancellare la memoria associata al segreto.</span><span class="sxs-lookup"><span data-stu-id="7d628-128">Clear the memory associated with the secret when done.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d628-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d628-129">Requirements</span></span>



| <span data-ttu-id="7d628-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d628-130">Requirement</span></span> | <span data-ttu-id="7d628-131">Valore</span><span class="sxs-lookup"><span data-stu-id="7d628-131">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d628-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7d628-132">End of client support</span></span><br/> | <span data-ttu-id="7d628-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d628-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7d628-134">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="7d628-134">End of server support</span></span><br/> | <span data-ttu-id="7d628-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d628-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7d628-136">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7d628-136">Redistributable</span></span><br/>       | <span data-ttu-id="7d628-137">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="7d628-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7d628-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7d628-138">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7d628-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d628-139"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d628-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d628-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d628-141">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="7d628-141">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="7d628-142">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="7d628-142">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
