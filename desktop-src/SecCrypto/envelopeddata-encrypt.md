---
description: Genera una chiave di sessione e crittografa i dati e le buste.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: Metodo EnvelopedData. Encrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecdb665a8e70ff329f25398eb855ff3e82c96cfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327093"
---
# <a name="envelopeddataencrypt-method"></a><span data-ttu-id="2f9f7-103">Metodo EnvelopedData. Encrypt</span><span class="sxs-lookup"><span data-stu-id="2f9f7-103">EnvelopedData.Encrypt method</span></span>

<span data-ttu-id="2f9f7-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2f9f7-105">Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="2f9f7-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="2f9f7-106">Il metodo **Encrypt** genera una chiave di sessione, USA tale chiave per crittografare il contenuto, racchiude il contenuto crittografato per ogni destinatario crittografando la chiave della sessione con la chiave pubblica di ogni destinatario, quindi restituisce il [*BLOB*](../secgloss/b-gly.md) che contiene il contenuto crittografato e le chiavi della sessione crittografata come stringa codificata.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-106">The **Encrypt** method generates a session key, uses that key to encrypt the contents, envelops the encrypted content for each recipient by encrypting the session key with each recipient's public key, and then returns the [*BLOB*](../secgloss/b-gly.md) that contains the encrypted contents and the encrypted session keys as an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f9f7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f9f7-107">Syntax</span></span>


```VB
EnvelopedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2f9f7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f9f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f9f7-109">*EncodingType* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2f9f7-109">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f9f7-110">Valore dell'enumerazione del [**\_ \_ tipo di codifica CAPICOM**](capicom-encoding-type.md) che indica il tipo di codifica utilizzato per codificare i dati in busta digitale.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-110">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the encoding type used to encode the enveloped data.</span></span> <span data-ttu-id="2f9f7-111">Il valore di codifica predefinito è CAPICOM \_ Encode \_ base64.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-111">The default encoding value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="2f9f7-112">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="2f9f7-113">Valore</span><span class="sxs-lookup"><span data-stu-id="2f9f7-113">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="2f9f7-114">Significato</span><span class="sxs-lookup"><span data-stu-id="2f9f7-114">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="2f9f7-115"><dt>**CAPICOM \_ Encode \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="2f9f7-115"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="2f9f7-116">Questo tipo di codifica viene utilizzato solo quando i dati di input hanno un tipo di codifica sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-116">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="2f9f7-117">Se questo valore viene usato per specificare il tipo di codifica dell'output, \_ \_ verrà invece usato CAPICOM Encode Base64.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-117">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="2f9f7-118">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-118">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="2f9f7-119"><dt>**\_Codifica Base64 per CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f9f7-119"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="2f9f7-120">I dati vengono salvati come stringa con codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-120">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="2f9f7-121"><dt>**\_codificare il \_ file binario di CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="2f9f7-121"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="2f9f7-122">I dati vengono salvati come una sequenza binaria pura.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-122">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f9f7-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f9f7-123">Return value</span></span>

<span data-ttu-id="2f9f7-124">Questo metodo restituisce un BLOB che contiene i dati in busta in una stringa codificata.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-124">This method returns a BLOB that contains the enveloped data in an encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f9f7-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f9f7-125">Remarks</span></span>

<span data-ttu-id="2f9f7-126">Il BLOB restituito contiene il contenuto crittografato e una chiave di sessione crittografata per ogni destinatario previsto.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-126">The returned BLOB contains the encrypted content and an encrypted session key for each intended recipient.</span></span> <span data-ttu-id="2f9f7-127">Queste chiavi di sessione vengono crittografate con la chiave pubblica di ogni destinatario.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-127">These session keys are encrypted using the public key of each recipient.</span></span> <span data-ttu-id="2f9f7-128">Le chiavi della sessione crittografata possono essere decrittografate solo con la chiave privata di un destinatario.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-128">The encrypted session keys can be decrypted only with a recipient's private key.</span></span>

<span data-ttu-id="2f9f7-129">Se la proprietà [**Recipients**](envelopeddata-recipients.md) non contiene informazioni, questo metodo cerca i destinatari potenziali nell'archivio certificati AddressBook dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-129">If the [**Recipients**](envelopeddata-recipients.md) property does not contain any information, this method searches the current user's AddressBook certificate store for potential recipients.</span></span> <span data-ttu-id="2f9f7-130">Se viene trovato più di un potenziale destinatario, all'utente viene richiesto di selezionare un destinatario da una finestra di dialogo di selezione.</span><span class="sxs-lookup"><span data-stu-id="2f9f7-130">If more than one potential recipient is found, the user is prompted to select a recipient from a selection dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f9f7-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f9f7-131">Requirements</span></span>



| <span data-ttu-id="2f9f7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f9f7-132">Requirement</span></span> | <span data-ttu-id="2f9f7-133">Valore</span><span class="sxs-lookup"><span data-stu-id="2f9f7-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f9f7-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2f9f7-134">End of client support</span></span><br/> | <span data-ttu-id="2f9f7-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f9f7-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2f9f7-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="2f9f7-136">End of server support</span></span><br/> | <span data-ttu-id="2f9f7-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f9f7-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2f9f7-138">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="2f9f7-138">Redistributable</span></span><br/>       | <span data-ttu-id="2f9f7-139">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="2f9f7-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2f9f7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2f9f7-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2f9f7-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f9f7-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f9f7-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f9f7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f9f7-143">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="2f9f7-143">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="2f9f7-144">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="2f9f7-144">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
