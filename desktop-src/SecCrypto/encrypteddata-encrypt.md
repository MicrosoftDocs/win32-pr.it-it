---
description: Deriva una chiave della sessione dal segreto e crittografa il valore della proprietà Content usando tale chiave. Restituisce il contenuto crittografato come stringa codificata.
ms.assetid: aa6f6e6a-208b-4e9c-b530-08673ab9d794
title: Metodo EncryptedData. Encrypt (infocard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 04d7bf8a337c1bcfa0a024b84304fe50c035f9dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324898"
---
# <a name="encrypteddataencrypt-method"></a><span data-ttu-id="bb227-104">Metodo EncryptedData. Encrypt</span><span class="sxs-lookup"><span data-stu-id="bb227-104">EncryptedData.Encrypt method</span></span>

<span data-ttu-id="bb227-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb227-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="bb227-106">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per crittografare e decrittografare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="bb227-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="bb227-107">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="bb227-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="bb227-108">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="bb227-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="bb227-109">Il metodo **Encrypt** deriva una chiave della sessione dal segreto e crittografa il valore della proprietà [**Content**](encrypteddata-content.md) usando tale chiave.</span><span class="sxs-lookup"><span data-stu-id="bb227-109">The **Encrypt** method derives a session key from the secret and encrypts the [**Content**](encrypteddata-content.md) property value using that key.</span></span> <span data-ttu-id="bb227-110">Restituisce il contenuto crittografato come stringa codificata.</span><span class="sxs-lookup"><span data-stu-id="bb227-110">It returns the encrypted content as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb227-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb227-111">Syntax</span></span>


```VB
EncryptedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="bb227-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb227-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb227-113">*EncodingType* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bb227-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bb227-114">Valore dell'enumerazione del [**\_ \_ tipo di codifica CAPICOM**](capicom-encoding-type.md) che indica il tipo di codifica utilizzato per codificare i dati crittografati.</span><span class="sxs-lookup"><span data-stu-id="bb227-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the encrypted data.</span></span> <span data-ttu-id="bb227-115">Il valore predefinito è CAPICOM \_ Encode \_ base64.</span><span class="sxs-lookup"><span data-stu-id="bb227-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="bb227-116">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bb227-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="bb227-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bb227-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="bb227-118">Significato</span><span class="sxs-lookup"><span data-stu-id="bb227-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="bb227-119"><dt>**CAPICOM \_ Encode \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="bb227-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="bb227-120">Questo tipo di codifica viene utilizzato solo quando i dati di input hanno un tipo di codifica sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="bb227-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="bb227-121">Se questo valore viene usato per specificare il tipo di codifica dell'output, \_ \_ verrà invece usato CAPICOM Encode Base64.</span><span class="sxs-lookup"><span data-stu-id="bb227-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="bb227-122">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="bb227-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="bb227-123"><dt>**\_Codifica Base64 per CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bb227-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="bb227-124">I dati vengono salvati come stringa con codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="bb227-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="bb227-125"><dt>**\_codificare il \_ file binario di CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="bb227-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="bb227-126">I dati vengono salvati come una sequenza binaria pura.</span><span class="sxs-lookup"><span data-stu-id="bb227-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb227-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb227-127">Return value</span></span>

<span data-ttu-id="bb227-128">Stringa che contiene i dati crittografati codificati.</span><span class="sxs-lookup"><span data-stu-id="bb227-128">A string that contains the encrypted, encoded data.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb227-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb227-129">Remarks</span></span>

<span data-ttu-id="bb227-130">Prima di chiamare il metodo **Encrypt** , impostare la proprietà [**Content**](encrypteddata-content.md) e chiamare il metodo [**sesecret**](encrypteddata-setsecret.md) .</span><span class="sxs-lookup"><span data-stu-id="bb227-130">Before calling the **Encrypt** method, set the [**Content**](encrypteddata-content.md) property and call the [**SetSecret**](encrypteddata-setsecret.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb227-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb227-131">Requirements</span></span>



| <span data-ttu-id="bb227-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb227-132">Requirement</span></span> | <span data-ttu-id="bb227-133">Valore</span><span class="sxs-lookup"><span data-stu-id="bb227-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb227-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bb227-134">End of client support</span></span><br/> | <span data-ttu-id="bb227-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb227-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bb227-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bb227-136">End of server support</span></span><br/> | <span data-ttu-id="bb227-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb227-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bb227-138">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="bb227-138">Redistributable</span></span><br/>       | <span data-ttu-id="bb227-139">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="bb227-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bb227-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb227-140">Header</span></span><br/>                | <dl> <span data-ttu-id="bb227-141"><dt>Infocard. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb227-141"><dt>Infocard.h</dt></span></span> </dl>  |
| <span data-ttu-id="bb227-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bb227-142">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bb227-143"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb227-143"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb227-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb227-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb227-145">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="bb227-145">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="bb227-146">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="bb227-146">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
