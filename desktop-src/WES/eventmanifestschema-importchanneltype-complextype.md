---
title: Tipo complesso ImportChannelType
description: Identifica un canale definito da un altro provider o in un manifesto che contiene una sezione di metadati.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- Log eventi di tipo complesso ImportChannelType
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7500d52179c3282c7f15dcdd5dd5a32620bbc076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119694"
---
# <a name="importchanneltype-complex-type"></a><span data-ttu-id="c79ec-104">Tipo complesso ImportChannelType</span><span class="sxs-lookup"><span data-stu-id="c79ec-104">ImportChannelType Complex Type</span></span>

<span data-ttu-id="c79ec-105">Identifica un canale definito da un altro provider o in un manifesto che contiene una sezione di metadati.</span><span class="sxs-lookup"><span data-stu-id="c79ec-105">Identifies a channel that has been defined by another provider or in a manifest that contains a metadata section.</span></span>

``` syntax
<xs:complexType name="ImportChannelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="chid"
                type="token"
                use="optional"
             />
            <xs:attribute name="name"
                type="anyURI"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="c79ec-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="c79ec-106">Attributes</span></span>



| <span data-ttu-id="c79ec-107">Nome</span><span class="sxs-lookup"><span data-stu-id="c79ec-107">Name</span></span>   | <span data-ttu-id="c79ec-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c79ec-108">Type</span></span>                                                              | <span data-ttu-id="c79ec-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c79ec-109">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c79ec-110">figlio</span><span class="sxs-lookup"><span data-stu-id="c79ec-110">chid</span></span>   | <span data-ttu-id="c79ec-111">token</span><span class="sxs-lookup"><span data-stu-id="c79ec-111">token</span></span>                                                             | <span data-ttu-id="c79ec-112">Identificatore che identifica in modo univoco il canale nell'elenco di canali che il provider definisce o importa.</span><span class="sxs-lookup"><span data-stu-id="c79ec-112">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="c79ec-113">Utilizzare questo valore quando si fa riferimento a questo canale in una definizione di evento.</span><span class="sxs-lookup"><span data-stu-id="c79ec-113">Use this value when referencing this channel in an event definition.</span></span> <span data-ttu-id="c79ec-114">Se non si specifica un identificatore di canale, utilizzare il nome del canale per fare riferimento a questo canale in una definizione di evento.</span><span class="sxs-lookup"><span data-stu-id="c79ec-114">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/>  |
| <span data-ttu-id="c79ec-115">name</span><span class="sxs-lookup"><span data-stu-id="c79ec-115">name</span></span>   | <span data-ttu-id="c79ec-116">anyURI</span><span class="sxs-lookup"><span data-stu-id="c79ec-116">anyURI</span></span>                                                            | <span data-ttu-id="c79ec-117">Nome del canale da importare.</span><span class="sxs-lookup"><span data-stu-id="c79ec-117">The name of the channel to import.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c79ec-118">simbolo</span><span class="sxs-lookup"><span data-stu-id="c79ec-118">symbol</span></span> | [<span data-ttu-id="c79ec-119">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="c79ec-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="c79ec-120">Simbolo da utilizzare per fare riferimento al canale nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c79ec-120">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="c79ec-121">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il canale nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="c79ec-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="c79ec-122">Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c79ec-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c79ec-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="c79ec-123">Remarks</span></span>

<span data-ttu-id="c79ec-124">Il manifesto che ha definito il canale importato deve essere installato prima che il provider scriva gli eventi; in caso contrario, gli eventi non possono essere scritti nel canale (l'operazione di scrittura ha esito positivo, gli eventi non vengono semplicemente scritti nel canale).</span><span class="sxs-lookup"><span data-stu-id="c79ec-124">The manifest that defined the imported channel must be installed before your provider writes events; otherwise, the events cannot be written to the channel (the write operation succeeds, the events are simply not written to the channel).</span></span>

## <a name="requirements"></a><span data-ttu-id="c79ec-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c79ec-125">Requirements</span></span>



| <span data-ttu-id="c79ec-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c79ec-126">Requirement</span></span> | <span data-ttu-id="c79ec-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c79ec-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c79ec-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c79ec-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c79ec-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c79ec-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c79ec-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c79ec-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c79ec-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c79ec-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





