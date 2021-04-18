---
description: Decrittografa una stringa di dati crittografata e codificata.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: Metodo EncryptedData. Decrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aa702a5cefc46f6d0cbe5d7e0fba17ff03596b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324901"
---
# <a name="encrypteddatadecrypt-method"></a><span data-ttu-id="9c991-103">Metodo EncryptedData. Decrypt</span><span class="sxs-lookup"><span data-stu-id="9c991-103">EncryptedData.Decrypt method</span></span>

<span data-ttu-id="9c991-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9c991-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9c991-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per crittografare e decrittografare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="9c991-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="9c991-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="9c991-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="9c991-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="9c991-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="9c991-108">Il metodo **Decrypt** decrittografa una stringa di dati crittografata e codificata.</span><span class="sxs-lookup"><span data-stu-id="9c991-108">The **Decrypt** method decrypts an encrypted and encoded data string.</span></span> <span data-ttu-id="9c991-109">I dati in testo non crittografato risultanti diventano la proprietà [**Content**](encrypteddata-content.md) dell'oggetto [**EncryptedData**](encrypteddata.md) .</span><span class="sxs-lookup"><span data-stu-id="9c991-109">The resulting plaintext data becomes the [**Content**](encrypteddata-content.md) property of the [**EncryptedData**](encrypteddata.md) object.</span></span> <span data-ttu-id="9c991-110">La decrittografia del contenuto ha esito negativo a meno che il segreto, impostato dal metodo [**sesecret**](encrypteddata-setsecret.md) , corrisponda esattamente a quello del segreto usato per derivare la chiave usata per crittografare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="9c991-110">Decryption of the content fails unless the secret, set by the [**SetSecret**](encrypteddata-setsecret.md) method, is exactly the same as the secret used to derive the key used to encrypt the content.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c991-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c991-111">Syntax</span></span>


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="9c991-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c991-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c991-113">*EncryptedMessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c991-113">*EncryptedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c991-114">Stringa che contiene i dati crittografati codificati da decrittografare.</span><span class="sxs-lookup"><span data-stu-id="9c991-114">String that contains the encoded, encrypted data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c991-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c991-115">Return value</span></span>

<span data-ttu-id="9c991-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9c991-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c991-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c991-117">Remarks</span></span>

<span data-ttu-id="9c991-118">La chiave della sessione derivata dal segreto corrente viene usata per la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="9c991-118">The session key derived from the current secret is used for the decryption.</span></span> <span data-ttu-id="9c991-119">Questo metodo non produrrà il testo non crittografato corretto, a meno che il segreto corrente corrisponda esattamente al segreto usato per crittografare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="9c991-119">This method will not produce the correct plaintext unless the current secret exactly matches the secret used to encrypt the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c991-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c991-120">Requirements</span></span>



| <span data-ttu-id="9c991-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c991-121">Requirement</span></span> | <span data-ttu-id="9c991-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9c991-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c991-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9c991-123">End of client support</span></span><br/> | <span data-ttu-id="9c991-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c991-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9c991-125">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="9c991-125">End of server support</span></span><br/> | <span data-ttu-id="9c991-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c991-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9c991-127">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9c991-127">Redistributable</span></span><br/>       | <span data-ttu-id="9c991-128">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="9c991-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9c991-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9c991-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9c991-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c991-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c991-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c991-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c991-132">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="9c991-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="9c991-133">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="9c991-133">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
