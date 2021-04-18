---
title: Tipo complesso ChannelListType
description: Definisce un elenco di canali a cui i provider possono registrare gli eventi. | Tipo complesso ChannelListType
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- Log eventi di tipo complesso ChannelListType
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53293687fd4ab0d87155b86edd026189f6d7c925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321939"
---
# <a name="channellisttype-complex-type"></a><span data-ttu-id="2434a-105">Tipo complesso ChannelListType</span><span class="sxs-lookup"><span data-stu-id="2434a-105">ChannelListType Complex Type</span></span>

<span data-ttu-id="2434a-106">Definisce un elenco di canali a cui i provider possono registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="2434a-106">Defines a list of channels to which providers can log events.</span></span>

``` syntax
<xs:complexType name="ChannelListType">
    <xs:choice
        minOccurs="0"
        maxOccurs="8"
    >
        <xs:element name="importChannel"
            type="ImportChannelType"
         />
        <xs:element name="channel"
            type="ChannelType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="2434a-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="2434a-107">Child elements</span></span>



| <span data-ttu-id="2434a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2434a-108">Element</span></span>                                                                            | <span data-ttu-id="2434a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2434a-109">Type</span></span>                                                                           | <span data-ttu-id="2434a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2434a-110">Description</span></span>                                                                                                                  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2434a-111">**canale**</span><span class="sxs-lookup"><span data-stu-id="2434a-111">**channel**</span></span>](eventmanifestschema-channel-channellisttype-element.md)             | [<span data-ttu-id="2434a-112">**ChannelType**</span><span class="sxs-lookup"><span data-stu-id="2434a-112">**ChannelType**</span></span>](eventmanifestschema-channeltype-complextype.md)             | <span data-ttu-id="2434a-113">Definisce un canale a cui è possibile registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="2434a-113">Defines a channel to which events can be logged.</span></span><br/>                                                                  |
| [<span data-ttu-id="2434a-114">**importChannel**</span><span class="sxs-lookup"><span data-stu-id="2434a-114">**importChannel**</span></span>](eventmanifestschema-importchannel-channellisttype-element.md) | [<span data-ttu-id="2434a-115">**ImportChannelType**</span><span class="sxs-lookup"><span data-stu-id="2434a-115">**ImportChannelType**</span></span>](eventmanifestschema-importchanneltype-complextype.md) | <span data-ttu-id="2434a-116">Identifica un canale definito da un altro provider o in un manifesto che contiene una sezione di metadati.</span><span class="sxs-lookup"><span data-stu-id="2434a-116">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2434a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2434a-117">Remarks</span></span>

<span data-ttu-id="2434a-118">È possibile specificare fino a otto canali (qualsiasi combinazione di canali o canali importati definiti).</span><span class="sxs-lookup"><span data-stu-id="2434a-118">You can specify up to eight channels (any combination of imported channels or channels that you define).</span></span>

## <a name="requirements"></a><span data-ttu-id="2434a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2434a-119">Requirements</span></span>



| <span data-ttu-id="2434a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2434a-120">Requirement</span></span> | <span data-ttu-id="2434a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2434a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2434a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2434a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2434a-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2434a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2434a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2434a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2434a-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2434a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





