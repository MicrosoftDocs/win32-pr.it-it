---
title: Tipo complesso IdentityPrivacyParameters
description: Contiene informazioni sull'utilizzo di identità anonime durante l'autenticazione PEAP.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8360065e2ce124531bec63637e2b6560cfc32f54
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104117253"
---
# <a name="identityprivacyparameters-complex-type"></a><span data-ttu-id="a40e4-103">Tipo complesso IdentityPrivacyParameters</span><span class="sxs-lookup"><span data-stu-id="a40e4-103">IdentityPrivacyParameters Complex Type</span></span>

<span data-ttu-id="a40e4-104">Il tipo complesso **IdentityPrivacyParameters** contiene informazioni sull'utilizzo di identità anonime durante l'autenticazione PEAP.</span><span class="sxs-lookup"><span data-stu-id="a40e4-104">The **IdentityPrivacyParameters** complex type contains information about anonymous identity usage during PEAP authentication.</span></span>


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| <span data-ttu-id="a40e4-105">Elemento</span><span class="sxs-lookup"><span data-stu-id="a40e4-105">Element</span></span>                                                                                                               | <span data-ttu-id="a40e4-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a40e4-106">Type</span></span>    | <span data-ttu-id="a40e4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a40e4-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a40e4-108">**EnableIdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="a40e4-108">**EnableIdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | <span data-ttu-id="a40e4-109">boolean</span><span class="sxs-lookup"><span data-stu-id="a40e4-109">boolean</span></span> | <span data-ttu-id="a40e4-110">Indica se viene inviata un'identità vera o anonima dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a40e4-110">Indicates whether a user's true identity or an anonymous identity is sent.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="a40e4-111">**AnonymousUserName**</span><span class="sxs-lookup"><span data-stu-id="a40e4-111">**AnonymousUserName**</span></span>](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | <span data-ttu-id="a40e4-112">string</span><span class="sxs-lookup"><span data-stu-id="a40e4-112">string</span></span>  | <span data-ttu-id="a40e4-113">contiene un'identità anonima utilizzata al posto dell'identificazione true di un utente.</span><span class="sxs-lookup"><span data-stu-id="a40e4-113">contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="a40e4-114">Viene inviato durante la prima fase dell'autenticazione PEAP quando l' **identità** viene inviata come testo normale.</span><span class="sxs-lookup"><span data-stu-id="a40e4-114">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span> <span data-ttu-id="a40e4-115">L'utilizzo dell'identità anonima è determinato dall'elemento [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a40e4-115">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a40e4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a40e4-116">Remarks</span></span>

<span data-ttu-id="a40e4-117">L'elemento IdentityPrivacyParameters è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a40e4-117">The IdentityPrivacyParameters element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a40e4-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a40e4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a40e4-119">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="a40e4-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a40e4-120">Schema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="a40e4-120">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="a40e4-121">Tipi complessi mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="a40e4-121">mspeapconnectionpropertiesv2 Complex Types</span></span>](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




