---
title: Elemento CredentialsBlob (EapHostUserCredentials)
description: Viene utilizzato quando la configurazione del metodo è un BLOB binario anziché in formato testo XML.
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- Elemento CredentialsBlob EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119343"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a><span data-ttu-id="a734b-104">Elemento CredentialsBlob (EapHostUserCredentials)</span><span class="sxs-lookup"><span data-stu-id="a734b-104">CredentialsBlob (EapHostUserCredentials) Element</span></span>

<span data-ttu-id="a734b-105">L'elemento **CredentialsBlob (EapHostUserCredentials)** viene utilizzato quando la configurazione del metodo è un BLOB binario anziché in formato testo XML.</span><span class="sxs-lookup"><span data-stu-id="a734b-105">The **CredentialsBlob (EapHostUserCredentials)** element is used when the method configuration is a binary BLOB instead of in XML text format.</span></span>

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="a734b-106">L'elemento **CredentialsBlob** è definito dall'elemento [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a734b-106">The **CredentialsBlob** element is defined by the [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a734b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="a734b-107">Remarks</span></span>

<span data-ttu-id="a734b-108">Gli elementi [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) e **CredentialsBlob** non possono essere usati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="a734b-108">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and **CredentialsBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="a734b-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a734b-109">Requirements</span></span>



| <span data-ttu-id="a734b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a734b-110">Requirement</span></span> | <span data-ttu-id="a734b-111">Valore</span><span class="sxs-lookup"><span data-stu-id="a734b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a734b-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a734b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a734b-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a734b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a734b-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a734b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a734b-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a734b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a734b-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a734b-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="a734b-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="a734b-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a734b-118">**EapHostUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="a734b-118">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

<span data-ttu-id="a734b-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="a734b-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a734b-120">**EapHostUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="a734b-120">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[<span data-ttu-id="a734b-121">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="a734b-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a734b-122">Schema eaphostusercredentials</span><span class="sxs-lookup"><span data-stu-id="a734b-122">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





