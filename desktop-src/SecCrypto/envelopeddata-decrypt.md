---
description: Decrittografa il contenuto in busta.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: Metodo EnvelopedData. Decrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c4c71ba0e3e0c2d421ad7bcbc9b1a61bb71d284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327897"
---
# <a name="envelopeddatadecrypt-method"></a><span data-ttu-id="29bdd-103">Metodo EnvelopedData. Decrypt</span><span class="sxs-lookup"><span data-stu-id="29bdd-103">EnvelopedData.Decrypt method</span></span>

<span data-ttu-id="29bdd-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="29bdd-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="29bdd-105">Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="29bdd-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="29bdd-106">Il metodo **Decrypt** decrittografa il contenuto in busta digitale.</span><span class="sxs-lookup"><span data-stu-id="29bdd-106">The **Decrypt** method decrypts enveloped content.</span></span> <span data-ttu-id="29bdd-107">La decrittografia viene eseguita se il destinatario del messaggio ha accesso alla [*chiave privata*](../secgloss/p-gly.md) associata a una delle [*chiavi pubbliche*](../secgloss/p-gly.md) usate per la busta del messaggio.</span><span class="sxs-lookup"><span data-stu-id="29bdd-107">Decryption is done if the recipient of the message has access to the [*private key*](../secgloss/p-gly.md) paired with one of the [*public keys*](../secgloss/p-gly.md) used to envelop the message.</span></span> <span data-ttu-id="29bdd-108">La chiamata al metodo **Decrypt** Reimposta lo [*stato*](../secgloss/s-gly.md) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="29bdd-108">Calling the **Decrypt** method resets the [*state*](../secgloss/s-gly.md) of the object.</span></span> <span data-ttu-id="29bdd-109">Se il metodo **Decrypt** ha esito positivo, la proprietà [**Content**](envelopeddata-content.md) dell'oggetto [**EnvelopedData**](envelopeddata.md) viene impostata sul messaggio in testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="29bdd-109">If the **Decrypt** method succeeds, the [**Content**](envelopeddata-content.md) property of the [**EnvelopedData**](envelopeddata.md) object is set to the plaintext message.</span></span>

## <a name="syntax"></a><span data-ttu-id="29bdd-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29bdd-110">Syntax</span></span>


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="29bdd-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="29bdd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29bdd-112">*EnvelopedMessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29bdd-112">*EnvelopedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29bdd-113">Stringa che contiene i dati in busta da decrittografare.</span><span class="sxs-lookup"><span data-stu-id="29bdd-113">String that contains the enveloped data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29bdd-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29bdd-114">Return value</span></span>

<span data-ttu-id="29bdd-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="29bdd-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29bdd-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="29bdd-116">Remarks</span></span>

<span data-ttu-id="29bdd-117">I dati decrittografati diventeranno il valore della proprietà [**Content**](envelopeddata-content.md) per l'oggetto [**EnvelopedData**](envelopeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="29bdd-117">The decrypted data becomes the [**Content**](envelopeddata-content.md) property value for the [**EnvelopedData**](envelopeddata.md) object.</span></span>

<span data-ttu-id="29bdd-118">Se l'utente di questo metodo non ha accesso a una chiave privata che corrisponde a una delle chiavi pubbliche usate per la busta del messaggio, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="29bdd-118">If the user of this method does not have access to a private key that matches one of the public keys used to envelop the message, the method fails.</span></span> <span data-ttu-id="29bdd-119">Questo metodo avrà esito negativo se il certificato per la chiave privata associata non si trova nell'archivio personale del computer locale o dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="29bdd-119">This method will fail if the certificate for the associated private key is not in either the local computer MY store or the current user MY store.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29bdd-120">Quando questo metodo viene chiamato da uno script Web, lo script deve usare la [*chiave privata*](../secgloss/p-gly.md) per decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="29bdd-120">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to decrypt the data.</span></span> <span data-ttu-id="29bdd-121">Consentire ai siti Web non attendibili di usare la chiave privata costituisce un rischio per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="29bdd-121">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="29bdd-122">Una finestra di dialogo in cui viene chiesto se il sito Web può utilizzare la chiave privata viene visualizzata quando questo metodo viene chiamato per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="29bdd-122">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="29bdd-123">Se si consente allo script di usare la chiave privata e selezionare "non visualizzare più questo messaggio", la finestra di dialogo non verrà più visualizzata per gli script che usano la chiave privata per decrittografare i dati all'interno del dominio.</span><span class="sxs-lookup"><span data-stu-id="29bdd-123">If you allow the script to use your private key and select "Do not ask me this again," the dialog box will no longer appear for any script that uses your private key to decrypt data within that domain.</span></span> <span data-ttu-id="29bdd-124">Tuttavia, gli script all'esterno del dominio che tentano di usare la chiave privata per decrittografare i dati continueranno a causare la visualizzazione di questa finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="29bdd-124">However, scripts outside that domain that attempt to use your private key to decrypt data will still cause this dialog box to appear.</span></span> <span data-ttu-id="29bdd-125">Se non si consente allo script di usare la chiave privata e selezionare "non visualizzare più questo messaggio", gli script all'interno di tale dominio verranno automaticamente rifiutati la possibilità di usare la chiave privata per decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="29bdd-125">If you do not allow the script to use your private key and select "Do not ask me this again," scripts within that domain will automatically be refused the ability to use your private key to decrypt data.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="29bdd-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29bdd-126">Requirements</span></span>



| <span data-ttu-id="29bdd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="29bdd-127">Requirement</span></span> | <span data-ttu-id="29bdd-128">Valore</span><span class="sxs-lookup"><span data-stu-id="29bdd-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29bdd-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="29bdd-129">End of client support</span></span><br/> | <span data-ttu-id="29bdd-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29bdd-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="29bdd-131">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="29bdd-131">End of server support</span></span><br/> | <span data-ttu-id="29bdd-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29bdd-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="29bdd-133">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="29bdd-133">Redistributable</span></span><br/>       | <span data-ttu-id="29bdd-134">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="29bdd-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="29bdd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="29bdd-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="29bdd-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29bdd-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29bdd-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29bdd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29bdd-138">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="29bdd-138">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="29bdd-139">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="29bdd-139">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
