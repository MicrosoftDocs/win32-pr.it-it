---
description: Imposta o recupera l'opzione del certificato del firmatario.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Proprietà Signer. Options
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c22cf7b9d9ebe7e98e534d62b0a2771391c6cacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330268"
---
# <a name="signeroptions-property"></a><span data-ttu-id="19d12-103">Proprietà Signer. Options</span><span class="sxs-lookup"><span data-stu-id="19d12-103">Signer.Options property</span></span>

<span data-ttu-id="19d12-104">\[La proprietà **options** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="19d12-104">\[The **Options** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="19d12-105">Usare invece la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="19d12-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="19d12-106">La proprietà **options** imposta o recupera l'opzione del certificato del firmatario.</span><span class="sxs-lookup"><span data-stu-id="19d12-106">The **Options** property sets or retrieves the signer's certificate option.</span></span>

<span data-ttu-id="19d12-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="19d12-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="19d12-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19d12-108">Syntax</span></span>


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a><span data-ttu-id="19d12-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="19d12-109">Property value</span></span>

<span data-ttu-id="19d12-110">Valore dell'enumerazione di [**\_ \_ \_ Opzioni di inclusione del certificato CAPICOM**](capicom-certificate-include-option.md) che specifica l'opzione del certificato del firmatario.</span><span class="sxs-lookup"><span data-stu-id="19d12-110">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies the signer's certificate option.</span></span> <span data-ttu-id="19d12-111">Il valore predefinito è la catena di \_ inclusione del certificato CApicol \_ \_ \_ ad eccezione della \_ radice.</span><span class="sxs-lookup"><span data-stu-id="19d12-111">The default value is CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT.</span></span> <span data-ttu-id="19d12-112">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="19d12-112">The following table shows the possible values.</span></span>



| <span data-ttu-id="19d12-113">Valore</span><span class="sxs-lookup"><span data-stu-id="19d12-113">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="19d12-114">Significato</span><span class="sxs-lookup"><span data-stu-id="19d12-114">Meaning</span></span>                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="19d12-115"><dt>**il certificato di \_ CAPICOM \_ include la \_ catena \_ ad eccezione della \_ radice**</dt></span><span class="sxs-lookup"><span data-stu-id="19d12-115"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="19d12-116">Salva tutti i certificati nella catena con l'eccezione dell'entità radice.</span><span class="sxs-lookup"><span data-stu-id="19d12-116">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="19d12-117"><dt>**il certificato di \_ CAPICOM \_ include l' \_ intera \_ catena**</dt></span><span class="sxs-lookup"><span data-stu-id="19d12-117"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="19d12-118">Salva la catena di certificati completa.</span><span class="sxs-lookup"><span data-stu-id="19d12-118">Saves the complete certificate chain.</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="19d12-119"><dt>**il certificato capicol \_ \_ include \_ \_ solo entità finale \_**</dt></span><span class="sxs-lookup"><span data-stu-id="19d12-119"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="19d12-120">Salva solo il certificato dell'entità finale.</span><span class="sxs-lookup"><span data-stu-id="19d12-120">Saves only the end entity certificate.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="19d12-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19d12-121">Requirements</span></span>



| <span data-ttu-id="19d12-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="19d12-122">Requirement</span></span> | <span data-ttu-id="19d12-123">Valore</span><span class="sxs-lookup"><span data-stu-id="19d12-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19d12-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="19d12-124">Redistributable</span></span><br/> | <span data-ttu-id="19d12-125">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="19d12-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="19d12-126">DLL</span><span class="sxs-lookup"><span data-stu-id="19d12-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="19d12-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19d12-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19d12-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19d12-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19d12-129">**Firmatario**</span><span class="sxs-lookup"><span data-stu-id="19d12-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
