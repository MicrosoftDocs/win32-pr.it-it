---
description: Imposta o Recupera il nome del CAPICOM dell'attributo. Si tratta della proprietà predefinita.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Proprietà Attribute.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f71bb231941765dd073d44abd11c56152ea2d975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324916"
---
# <a name="attributename-property"></a><span data-ttu-id="10546-104">Proprietà Attribute.Name</span><span class="sxs-lookup"><span data-stu-id="10546-104">Attribute.Name property</span></span>

<span data-ttu-id="10546-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="10546-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="10546-106">Usare invece la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="10546-106">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="10546-107">La proprietà **Name** imposta o Recupera il nome del CAPICOM dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="10546-107">The **Name** property sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="10546-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="10546-108">This is the default property.</span></span>

<span data-ttu-id="10546-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="10546-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="10546-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10546-110">Syntax</span></span>


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a><span data-ttu-id="10546-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="10546-111">Property value</span></span>

<span data-ttu-id="10546-112">Valore dell'enumerazione dell' [**\_ attributo CAPICOM**](capicom-attribute.md) che specifica il nome del CAPICOM dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="10546-112">A value of the [**CAPICOM\_ATTRIBUTE**](capicom-attribute.md) enumeration that specifies the CAPICOM name of the attribute.</span></span> <span data-ttu-id="10546-113">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="10546-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="10546-114">Valore</span><span class="sxs-lookup"><span data-stu-id="10546-114">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="10546-115">Significato</span><span class="sxs-lookup"><span data-stu-id="10546-115">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <span data-ttu-id="10546-116"><dt>**\_tempo di firma dell'attributo autenticato di CAPICOM \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="10546-116"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME**</dt></span></span> </dl>                         | <span data-ttu-id="10546-117">L'attributo contiene la data e l'ora di creazione della firma.</span><span class="sxs-lookup"><span data-stu-id="10546-117">The attribute contains the time that the signature was created.</span></span><br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <span data-ttu-id="10546-118"><dt>**\_nome del documento dell'attributo autenticato di CAPICOM \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="10546-118"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_NAME**</dt></span></span> </dl>                      | <span data-ttu-id="10546-119">L'attributo contiene il nome del documento firmato.</span><span class="sxs-lookup"><span data-stu-id="10546-119">The attribute contains the name of the signed document.</span></span><br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <span data-ttu-id="10546-120"><dt>**\_Descrizione del documento dell'attributo autenticato CAPICOM \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="10546-120"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_DESCRIPTION**</dt></span></span> </dl> | <span data-ttu-id="10546-121">L'attributo contiene una descrizione del documento firmato.</span><span class="sxs-lookup"><span data-stu-id="10546-121">The attribute contains a description of the signed document.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="10546-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="10546-122">Remarks</span></span>

<span data-ttu-id="10546-123">Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero stato dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="10546-123">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="10546-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10546-124">Requirements</span></span>



| <span data-ttu-id="10546-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="10546-125">Requirement</span></span> | <span data-ttu-id="10546-126">Valore</span><span class="sxs-lookup"><span data-stu-id="10546-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10546-127">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="10546-127">End of client support</span></span><br/> | <span data-ttu-id="10546-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10546-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="10546-129">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="10546-129">End of server support</span></span><br/> | <span data-ttu-id="10546-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10546-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="10546-131">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="10546-131">Redistributable</span></span><br/>       | <span data-ttu-id="10546-132">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="10546-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="10546-133">DLL</span><span class="sxs-lookup"><span data-stu-id="10546-133">DLL</span></span><br/>                   | <dl> <span data-ttu-id="10546-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10546-134"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10546-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10546-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10546-136">**Attributo**</span><span class="sxs-lookup"><span data-stu-id="10546-136">**Attribute**</span></span>](attribute.md)
</dt> </dl>

 

 
