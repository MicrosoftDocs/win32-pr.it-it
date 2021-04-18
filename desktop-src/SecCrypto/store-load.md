---
description: Importa i certificati da un file nell'archivio.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Store. Load (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 32261a6fd8c5cf4382832d8286d63ce5d44fb542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333873"
---
# <a name="storeload-method"></a><span data-ttu-id="3e5ed-103">Store. Load (metodo)</span><span class="sxs-lookup"><span data-stu-id="3e5ed-103">Store.Load method</span></span>

<span data-ttu-id="3e5ed-104">\[Il metodo **Load** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3e5ed-105">Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="3e5ed-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3e5ed-106">Il metodo **Load** importa i certificati da un file nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-106">The **Load** method imports certificates from a file into the store.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e5ed-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e5ed-107">Syntax</span></span>


```VB
Store.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="3e5ed-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e5ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e5ed-109">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e5ed-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e5ed-110">Stringa che contiene il percorso di un file con estensione cer, SST, SPC, p7s o pfx o qualsiasi file firmato Authenticode.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-110">The string that contains the path to a .cer, .sst, .spc, .p7s, or .pfx file, or any Authenticode signed file.</span></span>

</dd> <dt>

<span data-ttu-id="3e5ed-111">*Password* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3e5ed-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3e5ed-112">Stringa che contiene la password in testo non crittografato per il file.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-112">The string that contains the plaintext password to the file.</span></span> <span data-ttu-id="3e5ed-113">Per la password è possibile usare fino a 32 caratteri Unicode, incluso un carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="3e5ed-114">Per informazioni sulla protezione della password, vedere [gestione delle password](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="3e5ed-114">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e5ed-115">*KeyStorageFlag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3e5ed-115">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3e5ed-116">Valore dell'enumerazione del [**\_ \_ \_ flag di archiviazione della chiave CAPICOM**](capicom-key-storage-flag.md) che definisce i flag di archiviazione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-116">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="3e5ed-117">Il valore predefinito è CAPICOM \_ Key \_ storage \_ default.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-117">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="3e5ed-118">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-118">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3e5ed-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3e5ed-119">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="3e5ed-120">Significato</span><span class="sxs-lookup"><span data-stu-id="3e5ed-120">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="3e5ed-121"><dt>**archiviazione delle chiavi di CAPICOM \_ \_ \_ predefinite**</dt></span><span class="sxs-lookup"><span data-stu-id="3e5ed-121"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="3e5ed-122">Archiviazione chiavi predefinita.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-122">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="3e5ed-123"><dt>**\_archiviazione chiavi CAPICOM \_ \_ esportabile**</dt></span><span class="sxs-lookup"><span data-stu-id="3e5ed-123"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="3e5ed-124">La chiave è esportabile.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-124">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="3e5ed-125"><dt>**archiviazione delle chiavi di CAPICOM \_ \_ \_ protetta dall'utente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3e5ed-125"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="3e5ed-126">La chiave è protetta dall'utente.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-126">The key is user protected.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e5ed-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e5ed-127">Return value</span></span>

<span data-ttu-id="3e5ed-128">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e5ed-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e5ed-129">Remarks</span></span>

<span data-ttu-id="3e5ed-130">Se il metodo **Load** viene chiamato in un archivio di memoria, tutti i contenitori di chiavi creati verranno eliminati quando l'archivio di memoria viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-130">If the **Load** method is called on a memory store, any key containers that are created will be deleted when the memory store is deleted.</span></span> <span data-ttu-id="3e5ed-131">Se, ad esempio, un file con estensione PFX viene caricato in un archivio di memoria e successivamente aggiunto a un archivio di sistema, ad esempio archivio personale, dall'archivio memoria, il certificato nell'archivio personale non conterrà una chiave.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-131">For example, if a .pfx file is loaded into a memory store and later added to a system store (such as the My store) from the memory store, the certificate in the My store will not contain a key.</span></span> <span data-ttu-id="3e5ed-132">In questo caso, il file con estensione pfx deve essere caricato direttamente nell'archivio personale.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-132">In this case, the .pfx file should be loaded directly into the My store.</span></span>

<span data-ttu-id="3e5ed-133">Questo metodo genera CAPICOM \_ E \_ non \_ è consentito quando viene inserito nello script da un'applicazione basata sul Web.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-133">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="3e5ed-134">Se la password non riesce a decrittografare il file di chiave privata, è necessario eseguire una query sul [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) predefinito.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-134">If the password fails to decrypt the private key file, then the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) should be queried.</span></span> <span data-ttu-id="3e5ed-135">Se il CSP predefinito è il provider di crittografia di base di Microsoft e l'operazione di decrittografia ha esito negativo, l'operazione di decrittografia deve essere riprovata con il provider Microsoft Strong Cryptographic Provider o Microsoft Enhanced Cryptographic Provider, a seconda di quale sia disponibile.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-135">If the default CSP is the Microsoft Base Cryptographic Provider and the decrypt operation fails, then the decrypt operation should be tried again with the Microsoft Strong Cryptographic Provider or Microsoft Enhanced Cryptographic Provider, whichever is available.</span></span>

<span data-ttu-id="3e5ed-136">Se il certificato caricato nell'archivio è identico a quello già presente, il metodo **Load** eliminerà il certificato esistente dall'archivio e quindi aggiungerà il nuovo certificato.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-136">If the certificate being loaded into the store is the same as one that is already there, the **Load** method will delete the existing certificate from the store and then add the new certificate.</span></span> <span data-ttu-id="3e5ed-137">Il nuovo certificato erediterà le proprietà dal certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-137">The new certificate will inherit properties from the existing certificate.</span></span> <span data-ttu-id="3e5ed-138">Il contenitore di chiavi private esistente viene sostituito dal nuovo contenitore di chiavi private.</span><span class="sxs-lookup"><span data-stu-id="3e5ed-138">The existing private key container is replaced by the new private key container.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e5ed-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e5ed-139">Requirements</span></span>



| <span data-ttu-id="3e5ed-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e5ed-140">Requirement</span></span> | <span data-ttu-id="3e5ed-141">Valore</span><span class="sxs-lookup"><span data-stu-id="3e5ed-141">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e5ed-142">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="3e5ed-142">Redistributable</span></span><br/> | <span data-ttu-id="3e5ed-143">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e5ed-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3e5ed-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3e5ed-144">DLL</span></span><br/>             | <dl> <span data-ttu-id="3e5ed-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e5ed-145"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e5ed-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e5ed-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e5ed-147">**Store**</span><span class="sxs-lookup"><span data-stu-id="3e5ed-147">**Store**</span></span>](store.md)
</dt> </dl>

 

 
