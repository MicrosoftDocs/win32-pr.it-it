---
title: Elemento ServerNames (ServerValidationParameters) (PEAP)
description: Informazioni sull'elemento ServerNames (ServerValidationParameters). Questo elemento rappresenta un elenco di nomi di server delimitati da punti e virgola. | Elemento ServerNames (ServerValidationParameters) (PEAP)
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
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
ms.openlocfilehash: 40aa7ba317b7ba7c3f7a06cce87ef57c2906fe4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321278"
---
# <a name="servernames-servervalidationparameters-element-peap"></a><span data-ttu-id="257ee-106">Elemento ServerNames (ServerValidationParameters) (PEAP)</span><span class="sxs-lookup"><span data-stu-id="257ee-106">ServerNames (ServerValidationParameters) element (PEAP)</span></span>

<span data-ttu-id="257ee-107">L'elemento **serverNames (ServerValidationParameters)** rappresenta un elenco di nomi di server delimitati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="257ee-107">The **ServerNames (ServerValidationParameters)** element represents a list of semicolon delimited server names.</span></span>

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="257ee-108">L'elemento **serverNames** viene definito dal tipo complesso [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="257ee-108">The **ServerNames** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="257ee-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="257ee-109">Remarks</span></span>

<span data-ttu-id="257ee-110">Ogni nome di server è delimitato da punti e virgola e può essere rappresentato da espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="257ee-110">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <span data-ttu-id="257ee-111">L'elemento **serverNames** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="257ee-111">The **ServerNames** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="257ee-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="257ee-112">Requirements</span></span>



| <span data-ttu-id="257ee-113">Ruolo</span><span class="sxs-lookup"><span data-stu-id="257ee-113">Role</span></span> | <span data-ttu-id="257ee-114">Versione minima del sistema operativo supportata</span><span class="sxs-lookup"><span data-stu-id="257ee-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="257ee-115">Client</span><span class="sxs-lookup"><span data-stu-id="257ee-115">Client</span></span><br/> | <span data-ttu-id="257ee-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="257ee-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="257ee-117">Server</span><span class="sxs-lookup"><span data-stu-id="257ee-117">Server</span></span><br/> | <span data-ttu-id="257ee-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="257ee-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="257ee-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="257ee-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="257ee-120">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="257ee-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="257ee-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="257ee-121">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="257ee-122">**Possibili elementi padre immediati nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="257ee-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="257ee-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="257ee-123">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="257ee-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="257ee-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="257ee-125">EAPHost e schema legacy</span><span class="sxs-lookup"><span data-stu-id="257ee-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="257ee-126">Schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="257ee-126">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="257ee-127">Elementi dello schema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="257ee-127">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





