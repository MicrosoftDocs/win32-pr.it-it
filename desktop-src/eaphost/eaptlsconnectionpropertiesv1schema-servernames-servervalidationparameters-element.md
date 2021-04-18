---
title: Elemento ServerNames (ServerValidationParameters) (TLS)
description: Informazioni sull'elemento ServerNames (ServerValidationParameters). Questo elemento rappresenta un elenco di nomi di server delimitati da punti e virgola. | Elemento ServerNames (ServerValidationParameters) (TLS)
ms.assetid: c6cfcc67-4e6a-4bf0-87d9-37cc1d504598
keywords:
- Nomeservers (elemento EAPHost)
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef94bc650432c4fb87abf00a93841d0d4d42e965
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321827"
---
# <a name="servernames-servervalidationparameters-element-tls"></a><span data-ttu-id="717ab-106">Elemento ServerNames (ServerValidationParameters) (TLS)</span><span class="sxs-lookup"><span data-stu-id="717ab-106">ServerNames (ServerValidationParameters) element (TLS)</span></span>

<span data-ttu-id="717ab-107">L'elemento **serverNames (ServerValidationParameters)** rappresenta un elenco di nomi di server delimitati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="717ab-107">The **ServerNames (ServerValidationParameters)** element represents a list of semicolon delimited server names.</span></span>

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="717ab-108">L'elemento **serverNames** viene definito dal tipo complesso [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="717ab-108">The **ServerNames** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="717ab-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="717ab-109">Remarks</span></span>

<span data-ttu-id="717ab-110">Ogni nome di server è delimitato da punti e virgola e può essere rappresentato da espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="717ab-110">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <span data-ttu-id="717ab-111">L'elemento **serverNames** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="717ab-111">The **ServerNames** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="717ab-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="717ab-112">Requirements</span></span>



| <span data-ttu-id="717ab-113">Ruolo</span><span class="sxs-lookup"><span data-stu-id="717ab-113">Role</span></span> | <span data-ttu-id="717ab-114">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="717ab-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="717ab-115">Client</span><span class="sxs-lookup"><span data-stu-id="717ab-115">Client</span></span><br/> | <span data-ttu-id="717ab-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="717ab-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="717ab-117">Server</span><span class="sxs-lookup"><span data-stu-id="717ab-117">Server</span></span><br/> | <span data-ttu-id="717ab-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="717ab-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="717ab-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="717ab-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="717ab-120">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="717ab-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="717ab-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="717ab-121">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="717ab-122">**Possibili elementi padre immediati nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="717ab-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="717ab-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="717ab-123">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="717ab-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="717ab-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="717ab-125">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="717ab-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="717ab-126">Schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="717ab-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="717ab-127">Elementi dello schema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="717ab-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





