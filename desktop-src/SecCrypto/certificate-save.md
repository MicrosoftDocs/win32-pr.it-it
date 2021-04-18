---
description: Salva il certificato in un file.
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: 'Metodo ICertificate2:: Save'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327098"
---
# <a name="icertificate2save-method"></a><span data-ttu-id="9c28e-103">Metodo ICertificate2:: Save</span><span class="sxs-lookup"><span data-stu-id="9c28e-103">ICertificate2::Save method</span></span>

<span data-ttu-id="9c28e-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9c28e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9c28e-105">Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="9c28e-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9c28e-106">Il metodo **Save** Salva il certificato in un file.</span><span class="sxs-lookup"><span data-stu-id="9c28e-106">The **Save** method saves the certificate to a file.</span></span> <span data-ttu-id="9c28e-107">Questo metodo è stato introdotto in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="9c28e-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c28e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c28e-108">Syntax</span></span>


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9c28e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c28e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c28e-110">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c28e-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c28e-111">Stringa che contiene il nome del file di output in cui verrà salvato il certificato.</span><span class="sxs-lookup"><span data-stu-id="9c28e-111">A string that contains the name of the output file where the certificate will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="9c28e-112">*Password* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9c28e-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9c28e-113">Stringa che contiene la password in [*testo non crittografato*](../secgloss/p-gly.md) per un file di [*chiave privata*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9c28e-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="9c28e-114">La password può contenere fino a 32 caratteri Unicode, incluso un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="9c28e-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="9c28e-115">Per informazioni sulla protezione della password, vedere [gestione delle password](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="9c28e-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c28e-116">*SaveAs* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9c28e-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9c28e-117">Valore dell'enumerazione dei [**\_ \_ \_ \_ tipi Salva come del certificato CAPICOM**](capicom-certificate-save-as-type.md) che specifica il formato del file di output.</span><span class="sxs-lookup"><span data-stu-id="9c28e-117">A value of the [**CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE**](capicom-certificate-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="9c28e-118">Il valore predefinito è il **\_ certificato CAPICOM \_ Salva \_ come \_ CER**.</span><span class="sxs-lookup"><span data-stu-id="9c28e-118">The default is **CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**.</span></span> <span data-ttu-id="9c28e-119">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="9c28e-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="9c28e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9c28e-120">Value</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="9c28e-121">Significato</span><span class="sxs-lookup"><span data-stu-id="9c28e-121">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <span data-ttu-id="9c28e-122"><dt>**\_certificato CAPICOM \_ Salva \_ come \_ CER**</dt></span><span class="sxs-lookup"><span data-stu-id="9c28e-122"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</dt></span></span> </dl> | <span data-ttu-id="9c28e-123">Il file di output verrà formattato come file con estensione CER senza chiavi private salvate.</span><span class="sxs-lookup"><span data-stu-id="9c28e-123">The output file will be formatted as a .cer file with no private keys saved.</span></span><br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <span data-ttu-id="9c28e-124"><dt>**certificato capicol \_ \_ Salva \_ come \_ PFX**</dt></span><span class="sxs-lookup"><span data-stu-id="9c28e-124"><dt>**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</dt></span></span> </dl> | <span data-ttu-id="9c28e-125">Il file di output verrà formattato come file con estensione pfx (PKCS \# 12) e verranno salvate anche tutte le chiavi private associate esportabili.</span><span class="sxs-lookup"><span data-stu-id="9c28e-125">The output file will be formatted as a .pfx (PKCS \#12) file and any associated private keys that are exportable will also be saved.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9c28e-126">*IncludeOption* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="9c28e-126">*IncludeOption* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9c28e-127">Valore dell'enumerazione dell' [**\_ \_ \_ opzione Includi certificato CAPICOM**](capicom-certificate-include-option.md) che specifica il numero di certificati nella catena salvati nel file di output.</span><span class="sxs-lookup"><span data-stu-id="9c28e-127">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies how many certificates in the chain are saved to the output file.</span></span> <span data-ttu-id="9c28e-128">Il valore predefinito è il certificato capicol \_ \_ include \_ \_ solo l'entità end \_ .</span><span class="sxs-lookup"><span data-stu-id="9c28e-128">The default is CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY.</span></span> <span data-ttu-id="9c28e-129">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="9c28e-129">The following table shows the possible values.</span></span>



| <span data-ttu-id="9c28e-130">Valore</span><span class="sxs-lookup"><span data-stu-id="9c28e-130">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="9c28e-131">Significato</span><span class="sxs-lookup"><span data-stu-id="9c28e-131">Meaning</span></span>                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="9c28e-132"><dt>**il certificato di \_ CAPICOM \_ include la \_ catena \_ ad eccezione della \_ radice**</dt></span><span class="sxs-lookup"><span data-stu-id="9c28e-132"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="9c28e-133">Salva tutti i certificati nella catena con l'eccezione dell'entità radice</span><span class="sxs-lookup"><span data-stu-id="9c28e-133">Saves all certificates in the chain with the exception of the root entity</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="9c28e-134"><dt>**il certificato di \_ CAPICOM \_ include l' \_ intera \_ catena**</dt></span><span class="sxs-lookup"><span data-stu-id="9c28e-134"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="9c28e-135">Salva la catena di certificati completa</span><span class="sxs-lookup"><span data-stu-id="9c28e-135">Saves the complete certificate chain</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="9c28e-136"><dt>**il certificato capicol \_ \_ include \_ \_ solo entità finale \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9c28e-136"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="9c28e-137">Salva solo il certificato di entità finale</span><span class="sxs-lookup"><span data-stu-id="9c28e-137">Saves only the end entity certificate</span></span><br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c28e-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c28e-138">Return value</span></span>

<span data-ttu-id="9c28e-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9c28e-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c28e-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c28e-140">Remarks</span></span>

<span data-ttu-id="9c28e-141">Questo metodo genera CAPICOM \_ E \_ non \_ è consentito quando viene inserito nello script da un'applicazione basata sul Web.</span><span class="sxs-lookup"><span data-stu-id="9c28e-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c28e-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c28e-142">Requirements</span></span>



| <span data-ttu-id="9c28e-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c28e-143">Requirement</span></span> | <span data-ttu-id="9c28e-144">Valore</span><span class="sxs-lookup"><span data-stu-id="9c28e-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c28e-145">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9c28e-145">End of client support</span></span><br/> | <span data-ttu-id="9c28e-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c28e-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9c28e-147">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="9c28e-147">End of server support</span></span><br/> | <span data-ttu-id="9c28e-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c28e-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9c28e-149">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9c28e-149">Redistributable</span></span><br/>       | <span data-ttu-id="9c28e-150">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="9c28e-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9c28e-151">DLL</span><span class="sxs-lookup"><span data-stu-id="9c28e-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9c28e-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c28e-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
