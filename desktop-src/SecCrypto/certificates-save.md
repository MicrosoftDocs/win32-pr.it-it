---
description: Salva gli oggetti certificato nella raccolta.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Metodo Certificates. Save
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36ab04b394bddcd829d9f15e7562b72125388d33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333163"
---
# <a name="certificatessave-method"></a><span data-ttu-id="b372a-103">Metodo Certificates. Save</span><span class="sxs-lookup"><span data-stu-id="b372a-103">Certificates.Save method</span></span>

<span data-ttu-id="b372a-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b372a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b372a-105">Usare invece la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b372a-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b372a-106">Il metodo **Save** Salva gli oggetti [**certificato**](certificate.md) nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="b372a-106">The **Save** method saves the [**Certificate**](certificate.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b372a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b372a-107">Syntax</span></span>


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b372a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b372a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b372a-109">*Nome file* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b372a-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b372a-110">Stringa che contiene il nome del file di output in cui verranno salvati i certificati.</span><span class="sxs-lookup"><span data-stu-id="b372a-110">A string that contains the name of the output file where the certificates will be saved.</span></span>

</dd> <dt>

<span data-ttu-id="b372a-111">*Password* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b372a-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b372a-112">Stringa che contiene la password in [*testo non crittografato*](../secgloss/p-gly.md) per un file di [*chiave privata*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b372a-112">A string that contains the [*plaintext*](../secgloss/p-gly.md) password for a [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="b372a-113">Il valore predefinito è una stringa vuota ("").</span><span class="sxs-lookup"><span data-stu-id="b372a-113">The default value is the empty string ("").</span></span> <span data-ttu-id="b372a-114">Per la password è possibile usare fino a 32 caratteri Unicode, incluso un carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="b372a-114">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="b372a-115">Per informazioni sulla protezione della password, vedere [gestione delle password](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="b372a-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="b372a-116">*SaveAs* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b372a-116">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b372a-117">Valore dell'enumerazione del [**tipo di certificato CApicol \_ \_ Salva \_ come \_**](capicom-certificates-save-as-type.md) che specifica il formato del file di output.</span><span class="sxs-lookup"><span data-stu-id="b372a-117">A value of the [**CAPICOM\_CERTIFICATES\_SAVE\_AS\_TYPE**](capicom-certificates-save-as-type.md) enumeration that specifies the format of the output file.</span></span> <span data-ttu-id="b372a-118">Il valore predefinito è i \_ certificati CAPICOM \_ Salva \_ come \_ PFX.</span><span class="sxs-lookup"><span data-stu-id="b372a-118">The default is CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX.</span></span> <span data-ttu-id="b372a-119">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="b372a-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="b372a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b372a-120">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="b372a-121">Significato</span><span class="sxs-lookup"><span data-stu-id="b372a-121">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <span data-ttu-id="b372a-122"><dt>**\_certificati CAPICOM \_ Salva \_ come \_ PFX**</dt></span><span class="sxs-lookup"><span data-stu-id="b372a-122"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PFX**</dt></span></span> </dl>                      | <span data-ttu-id="b372a-123">I certificati vengono salvati come PFX.</span><span class="sxs-lookup"><span data-stu-id="b372a-123">The certificates are saved as a PFX.</span></span><br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <span data-ttu-id="b372a-124"><dt>**I certificati CAPICOM \_ vengono \_ salvati \_ come \_ PKCS7**</dt></span><span class="sxs-lookup"><span data-stu-id="b372a-124"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="b372a-125">I certificati vengono salvati come PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="b372a-125">The certificates are saved as a PKCS \#7.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <span data-ttu-id="b372a-126"><dt>**i certificati CAPICOM \_ vengono \_ salvati \_ come \_ serializzati**</dt></span><span class="sxs-lookup"><span data-stu-id="b372a-126"><dt>**CAPICOM\_CERTIFICATES\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="b372a-127">I certificati vengono salvati come serializzati.</span><span class="sxs-lookup"><span data-stu-id="b372a-127">The certificates are saved as serialized.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b372a-128">*ExportFlag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b372a-128">*ExportFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b372a-129">Valore dell'enumerazione del [**\_ \_ flag di esportazione CAPICOM**](capicom-export-flag.md) che specifica se eventuali errori di esportazione della chiave privata vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="b372a-129">A value of the [**CAPICOM\_EXPORT\_FLAG**](capicom-export-flag.md) enumeration that specifies whether any private key export errors are ignored.</span></span> <span data-ttu-id="b372a-130">Il valore predefinito è CAPICOM \_ Export \_ default.</span><span class="sxs-lookup"><span data-stu-id="b372a-130">The default is CAPICOM\_EXPORT\_DEFAULT.</span></span> <span data-ttu-id="b372a-131">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="b372a-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="b372a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b372a-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="b372a-133">Significato</span><span class="sxs-lookup"><span data-stu-id="b372a-133">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <span data-ttu-id="b372a-134"><dt>**impostazione predefinita per l'esportazione di CAPICOM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b372a-134"><dt>**CAPICOM\_EXPORT\_DEFAULT**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="b372a-135">Gli errori di esportazione della chiave privata non vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="b372a-135">Private key export errors are not ignored.</span></span><br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <span data-ttu-id="b372a-136"><dt>**errore di esportazione di CAPICOM \_ \_ Ignora \_ \_ chiave privata \_ non \_ esportabile \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b372a-136"><dt>**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="b372a-137">Gli errori di esportazione della chiave privata vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="b372a-137">Private key export errors are ignored.</span></span><br/>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b372a-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b372a-138">Return value</span></span>

<span data-ttu-id="b372a-139">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b372a-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b372a-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="b372a-140">Remarks</span></span>

<span data-ttu-id="b372a-141">Questo metodo genera CAPICOM \_ E \_ non \_ è consentito quando viene inserito nello script da un'applicazione basata sul Web.</span><span class="sxs-lookup"><span data-stu-id="b372a-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="b372a-142">È possibile recuperare gli oggetti [**certificato**](certificate.md) tramite il metodo [**Store. Load**](store-load.md) .</span><span class="sxs-lookup"><span data-stu-id="b372a-142">The [**Certificate**](certificate.md) objects can be retrieved by using the [**Store.Load**](store-load.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b372a-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b372a-143">Requirements</span></span>



| <span data-ttu-id="b372a-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="b372a-144">Requirement</span></span> | <span data-ttu-id="b372a-145">Valore</span><span class="sxs-lookup"><span data-stu-id="b372a-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b372a-146">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b372a-146">End of client support</span></span><br/> | <span data-ttu-id="b372a-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b372a-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b372a-148">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b372a-148">End of server support</span></span><br/> | <span data-ttu-id="b372a-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b372a-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b372a-150">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b372a-150">Redistributable</span></span><br/>       | <span data-ttu-id="b372a-151">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="b372a-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b372a-152">DLL</span><span class="sxs-lookup"><span data-stu-id="b372a-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b372a-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b372a-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b372a-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b372a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b372a-155">**Certificati**</span><span class="sxs-lookup"><span data-stu-id="b372a-155">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
