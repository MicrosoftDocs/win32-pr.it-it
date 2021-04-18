---
description: Importa un certificato da un file.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: 'Metodo ICertificate2:: Load'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9193297ad7eacc1994e4bf3729a87054573b1574
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324409"
---
# <a name="icertificate2load-method"></a><span data-ttu-id="bc2e9-103">Metodo ICertificate2:: Load</span><span class="sxs-lookup"><span data-stu-id="bc2e9-103">ICertificate2::Load method</span></span>

<span data-ttu-id="bc2e9-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="bc2e9-105">Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="bc2e9-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bc2e9-106">Il metodo **Load** importa un certificato da un file.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-106">The **Load** method imports a certificate from a file.</span></span> <span data-ttu-id="bc2e9-107">Questo metodo è stato introdotto in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc2e9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc2e9-108">Syntax</span></span>


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a><span data-ttu-id="bc2e9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc2e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc2e9-110">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc2e9-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc2e9-111">Stringa che contiene il percorso di un file con estensione cer o PFX che contiene i dati del certificato.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-111">A string that contains the path to a .cer or .pfx file that contains the certificate data.</span></span>

</dd> <dt>

<span data-ttu-id="bc2e9-112">*Password* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bc2e9-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bc2e9-113">Stringa che contiene la password in [*testo non crittografato*](../secgloss/p-gly.md) per il file di [*chiave privata*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bc2e9-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password to the [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="bc2e9-114">La password può contenere fino a 32 caratteri Unicode, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="bc2e9-115">Per informazioni sulla protezione della password, vedere [gestione delle password](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="bc2e9-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc2e9-116">*KeyStorageFlag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bc2e9-116">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bc2e9-117">Valore dell'enumerazione del [**\_ \_ \_ flag di archiviazione della chiave CAPICOM**](capicom-key-storage-flag.md) che definisce i flag di archiviazione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-117">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="bc2e9-118">Il valore predefinito è CAPICOM \_ Key \_ storage \_ default.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-118">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="bc2e9-119">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="bc2e9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="bc2e9-120">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="bc2e9-121">Significato</span><span class="sxs-lookup"><span data-stu-id="bc2e9-121">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="bc2e9-122"><dt>**archiviazione delle chiavi di CAPICOM \_ \_ \_ predefinite**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e9-122"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="bc2e9-123">Archiviazione chiavi predefinita.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-123">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="bc2e9-124"><dt>**\_archiviazione chiavi CAPICOM \_ \_ esportabile**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e9-124"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="bc2e9-125">La chiave è esportabile.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-125">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="bc2e9-126"><dt>**archiviazione delle chiavi di CAPICOM \_ \_ \_ protetta dall'utente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e9-126"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="bc2e9-127">La chiave è protetta dall'utente.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-127">The key is user protected.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bc2e9-128">*Posizione della sede* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bc2e9-128">*KeyLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bc2e9-129">Valore dell'enumerazione del [**\_ \_ percorso della chiave CAPICOM**](capicom-key-location.md) che definisce i tipi di posizione chiave.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-129">A value of the [**CAPICOM\_KEY\_LOCATION**](capicom-key-location.md) enumeration that defines key location types.</span></span> <span data-ttu-id="bc2e9-130">Il valore predefinito è CAPICOM \_ \_ chiave utente corrente \_ .</span><span class="sxs-lookup"><span data-stu-id="bc2e9-130">The default value is CAPICOM\_CURRENT\_USER\_KEY.</span></span> <span data-ttu-id="bc2e9-131">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="bc2e9-132">Valore</span><span class="sxs-lookup"><span data-stu-id="bc2e9-132">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="bc2e9-133">Significato</span><span class="sxs-lookup"><span data-stu-id="bc2e9-133">Meaning</span></span>                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <span data-ttu-id="bc2e9-134"><dt>**\_ \_ chiave utente corrente di CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e9-134"><dt>**CAPICOM\_CURRENT\_USER\_KEY**</dt></span></span> </dl>    | <span data-ttu-id="bc2e9-135">La chiave è una chiave utente.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-135">The key is a user key.</span></span><br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <span data-ttu-id="bc2e9-136"><dt>**\_chiave del computer locale \_ CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e9-136"><dt>**CAPICOM\_LOCAL\_MACHINE\_KEY**</dt></span></span> </dl> | <span data-ttu-id="bc2e9-137">La chiave è una chiave del computer.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-137">The key is a machine key.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc2e9-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc2e9-138">Return value</span></span>

<span data-ttu-id="bc2e9-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc2e9-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc2e9-140">Remarks</span></span>

<span data-ttu-id="bc2e9-141">Questo metodo genera CAPICOM \_ E \_ non \_ è consentito quando viene inserito nello script da un'applicazione basata sul Web.</span><span class="sxs-lookup"><span data-stu-id="bc2e9-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc2e9-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc2e9-142">Requirements</span></span>



| <span data-ttu-id="bc2e9-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc2e9-143">Requirement</span></span> | <span data-ttu-id="bc2e9-144">Valore</span><span class="sxs-lookup"><span data-stu-id="bc2e9-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc2e9-145">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bc2e9-145">End of client support</span></span><br/> | <span data-ttu-id="bc2e9-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc2e9-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bc2e9-147">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bc2e9-147">End of server support</span></span><br/> | <span data-ttu-id="bc2e9-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc2e9-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bc2e9-149">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="bc2e9-149">Redistributable</span></span><br/>       | <span data-ttu-id="bc2e9-150">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="bc2e9-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bc2e9-151">DLL</span><span class="sxs-lookup"><span data-stu-id="bc2e9-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bc2e9-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc2e9-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
