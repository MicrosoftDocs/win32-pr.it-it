---
description: Definisce il tipo di attributo associato a una firma.
ms.assetid: 94f0dce4-0b32-4c39-ab2e-b01795432acd
title: Enumerazione CAPICOM_ATTRIBUTE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ATTRIBUTE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: b03f91d0737b29b98adeb7e6a56bf9eccd35cc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331782"
---
# <a name="capicom_attribute-enumeration"></a><span data-ttu-id="b2bd6-103">\_Enumerazione dell'attributo CAPICOM</span><span class="sxs-lookup"><span data-stu-id="b2bd6-103">CAPICOM\_ATTRIBUTE enumeration</span></span>

<span data-ttu-id="b2bd6-104">Il tipo di enumerazione dell' **\_ attributo CAPICOM** definisce il tipo di attributo associato a una [*firma*](../secgloss/d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b2bd6-104">The **CAPICOM\_ATTRIBUTE** enumeration type defines the kind of attribute associated with a [*signature*](../secgloss/d-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="b2bd6-105">Membri</span><span class="sxs-lookup"><span data-stu-id="b2bd6-105">Members</span></span>



| <span data-ttu-id="b2bd6-106">Membro</span><span class="sxs-lookup"><span data-stu-id="b2bd6-106">Member</span></span>                                                       | <span data-ttu-id="b2bd6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2bd6-107">Description</span></span>                                                                | <span data-ttu-id="b2bd6-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b2bd6-108">Value</span></span> |
|--------------------------------------------------------------|----------------------------------------------------------------------------|-------|
| <span data-ttu-id="b2bd6-109">**\_tempo di firma dell'attributo autenticato di CAPICOM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b2bd6-109">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME**</span></span>         | <span data-ttu-id="b2bd6-110">L'attributo contiene la data e l'ora di creazione della firma.</span><span class="sxs-lookup"><span data-stu-id="b2bd6-110">The attribute contains the time that the signature was created.</span></span><br/> | <span data-ttu-id="b2bd6-111">0</span><span class="sxs-lookup"><span data-stu-id="b2bd6-111">0</span></span>     |
| <span data-ttu-id="b2bd6-112">**\_nome del documento dell'attributo autenticato di CAPICOM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b2bd6-112">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_NAME**</span></span>        | <span data-ttu-id="b2bd6-113">L'attributo contiene il nome del documento firmato.</span><span class="sxs-lookup"><span data-stu-id="b2bd6-113">The attribute contains the name of the signed document.</span></span><br/>         | <span data-ttu-id="b2bd6-114">1</span><span class="sxs-lookup"><span data-stu-id="b2bd6-114">1</span></span>     |
| <span data-ttu-id="b2bd6-115">**\_Descrizione del documento dell'attributo autenticato CAPICOM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b2bd6-115">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_DESCRIPTION**</span></span> | <span data-ttu-id="b2bd6-116">L'attributo contiene una descrizione del documento firmato.</span><span class="sxs-lookup"><span data-stu-id="b2bd6-116">The attribute contains a description of the signed document.</span></span><br/>    | <span data-ttu-id="b2bd6-117">2</span><span class="sxs-lookup"><span data-stu-id="b2bd6-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="b2bd6-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2bd6-118">Remarks</span></span>

<span data-ttu-id="b2bd6-119">Il tipo di enumerazione dell' **\_ attributo CAPICOM** viene usato dalla proprietà [**Attribute.Name**](attribute-name.md) .</span><span class="sxs-lookup"><span data-stu-id="b2bd6-119">The **CAPICOM\_ATTRIBUTE** enumeration type is used by the [**Attribute.Name**](attribute-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2bd6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2bd6-120">Requirements</span></span>



| <span data-ttu-id="b2bd6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2bd6-121">Requirement</span></span> | <span data-ttu-id="b2bd6-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b2bd6-122">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b2bd6-123">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b2bd6-123">Redistributable</span></span><br/> | <span data-ttu-id="b2bd6-124">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="b2bd6-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="b2bd6-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2bd6-125">Header</span></span><br/>          | <dl> <span data-ttu-id="b2bd6-126"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2bd6-126"><dt>Capicom.h</dt></span></span> </dl> |



 

 
