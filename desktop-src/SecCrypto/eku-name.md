---
description: Imposta o recupera un valore di enumerazione che specifica il nome di CAPICOM dell'EKU. Si tratta della proprietà predefinita.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: 'Proprietà IEKU:: Name'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330912"
---
# <a name="iekuname-property"></a><span data-ttu-id="4bceb-104">Proprietà IEKU:: Name</span><span class="sxs-lookup"><span data-stu-id="4bceb-104">IEKU::Name property</span></span>

<span data-ttu-id="4bceb-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4bceb-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4bceb-106">Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4bceb-106">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4bceb-107">La proprietà **Name** imposta o recupera un valore di enumerazione che specifica il nome di CAPICOM dell'EKU.</span><span class="sxs-lookup"><span data-stu-id="4bceb-107">The **Name** property sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="4bceb-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="4bceb-108">This is the default property.</span></span>

<span data-ttu-id="4bceb-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4bceb-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bceb-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4bceb-110">Syntax</span></span>


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a><span data-ttu-id="4bceb-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4bceb-111">Property value</span></span>

<span data-ttu-id="4bceb-112">Valore dell'enumerazione [**\_ EKU di CAPICOM**](capicom-eku.md) che specifica il nome di CAPICOM dell'EKU.</span><span class="sxs-lookup"><span data-stu-id="4bceb-112">A value of the [**CAPICOM\_EKU**](capicom-eku.md) enumeration that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="4bceb-113">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="4bceb-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="4bceb-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4bceb-114">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="4bceb-115">Significato</span><span class="sxs-lookup"><span data-stu-id="4bceb-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <span data-ttu-id="4bceb-116"><dt>**\_altro EKU di CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bceb-116"><dt>**CAPICOM\_EKU\_OTHER**</dt></span></span> </dl>                                                      | <span data-ttu-id="4bceb-117">Il certificato ha usi definiti nei criteri locali.</span><span class="sxs-lookup"><span data-stu-id="4bceb-117">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="4bceb-118">Viene usato se l'EKU necessario non è predefinito e il valore OID deve essere impostato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4bceb-118">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <span data-ttu-id="4bceb-119"><dt>**\_ \_ autenticazione server EKU CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bceb-119"><dt>**CAPICOM\_EKU\_SERVER\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="4bceb-120">Il certificato può essere usato per autenticare un server.</span><span class="sxs-lookup"><span data-stu-id="4bceb-120">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <span data-ttu-id="4bceb-121"><dt>**\_ \_ autenticazione client EKU CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bceb-121"><dt>**CAPICOM\_EKU\_CLIENT\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="4bceb-122">Il certificato può essere usato per autenticare un client.</span><span class="sxs-lookup"><span data-stu-id="4bceb-122">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <span data-ttu-id="4bceb-123"><dt>**\_firma del codice EKU \_ di \_ CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="4bceb-123"><dt>**CAPICOM\_EKU\_CODE\_SIGNING**</dt></span></span> </dl>                                | <span data-ttu-id="4bceb-124">Il certificato può essere usato per creare una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="4bceb-124">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <span data-ttu-id="4bceb-125"><dt>**\_ \_ protezione della posta elettronica EKU di CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bceb-125"><dt>**CAPICOM\_EKU\_EMAIL\_PROTECTION**</dt></span></span> </dl>                    | <span data-ttu-id="4bceb-126">Il certificato può essere usato per la protezione della posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="4bceb-126">Certificate can be used for email protection.</span></span><br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <span data-ttu-id="4bceb-127"><dt>**\_ \_ accesso smart card EKU CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bceb-127"><dt>**CAPICOM\_EKU\_SMARTCARD\_LOGON**</dt></span></span> </dl>                       | <span data-ttu-id="4bceb-128">È possibile utilizzare il certificato per l'accesso con smart card.</span><span class="sxs-lookup"><span data-stu-id="4bceb-128">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="4bceb-129">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="4bceb-129">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <span data-ttu-id="4bceb-130"><dt>**\_crittografia EKU del \_ \_ file \_ System per CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="4bceb-130"><dt>**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</dt></span></span> </dl> | <span data-ttu-id="4bceb-131">Il certificato può essere usato per EFS.</span><span class="sxs-lookup"><span data-stu-id="4bceb-131">Certificate can be used for EFS.</span></span> <span data-ttu-id="4bceb-132">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="4bceb-132">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="4bceb-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="4bceb-133">Remarks</span></span>

<span data-ttu-id="4bceb-134">Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4bceb-134">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bceb-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bceb-135">Requirements</span></span>



| <span data-ttu-id="4bceb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bceb-136">Requirement</span></span> | <span data-ttu-id="4bceb-137">Valore</span><span class="sxs-lookup"><span data-stu-id="4bceb-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bceb-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4bceb-138">End of client support</span></span><br/> | <span data-ttu-id="4bceb-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4bceb-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4bceb-140">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4bceb-140">End of server support</span></span><br/> | <span data-ttu-id="4bceb-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bceb-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4bceb-142">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4bceb-142">Redistributable</span></span><br/>       | <span data-ttu-id="4bceb-143">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="4bceb-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4bceb-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4bceb-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4bceb-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bceb-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
