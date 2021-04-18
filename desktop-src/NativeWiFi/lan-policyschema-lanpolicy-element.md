---
description: Contiene un criterio LAN cablata.
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: Elemento LANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b424a47405aa8f32276019a85902bd51b173cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314761"
---
# <a name="lanpolicy-element"></a><span data-ttu-id="5c5cc-103">Elemento LANPolicy</span><span class="sxs-lookup"><span data-stu-id="5c5cc-103">LANPolicy Element</span></span>

<span data-ttu-id="5c5cc-104">L'elemento LANPolicy contiene un criterio LAN cablata.</span><span class="sxs-lookup"><span data-stu-id="5c5cc-104">The LANPolicy element contains a wired LAN policy.</span></span> <span data-ttu-id="5c5cc-105">Questo elemento è l'elemento radice univoco per un profilo di criteri di rete cablata.</span><span class="sxs-lookup"><span data-stu-id="5c5cc-105">This element is the unique root element for a wired network policy profile.</span></span>

<span data-ttu-id="5c5cc-106">Lo spazio dei nomi di destinazione per l'elemento **LANPolicy** è `https://www.microsoft.com/networking/LAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="5c5cc-106">The target namespace for the **LANPolicy** element is `https://www.microsoft.com/networking/LAN/policy/v1`.</span></span>

``` syntax
<xs:element name="LANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="5c5cc-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5c5cc-107">Child elements</span></span>



| <span data-ttu-id="5c5cc-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5c5cc-108">Element</span></span>                                                                           | <span data-ttu-id="5c5cc-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c5cc-109">Type</span></span>                                                     | <span data-ttu-id="5c5cc-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c5cc-110">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c5cc-111">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5c5cc-111">**description**</span></span>](lan-policyschema-description-lanpolicy-element.md)             | [<span data-ttu-id="5c5cc-112">**nameType**</span><span class="sxs-lookup"><span data-stu-id="5c5cc-112">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="5c5cc-113">Contiene la descrizione di un criterio LAN cablata.</span><span class="sxs-lookup"><span data-stu-id="5c5cc-113">Contains the description of a wired LAN policy.</span></span> <br/>                                                                                                                          |
| [<span data-ttu-id="5c5cc-114">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="5c5cc-114">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="5c5cc-115">boolean</span><span class="sxs-lookup"><span data-stu-id="5c5cc-115">boolean</span></span>                                                  | <span data-ttu-id="5c5cc-116">Specifica se i computer utilizzano il servizio di configurazione automatica incorporato per gestire le connessioni a reti cablate che richiedono l'autenticazione di livello 2, ad esempio 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="5c5cc-116">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |
| [<span data-ttu-id="5c5cc-117">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="5c5cc-117">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | <span data-ttu-id="5c5cc-118">Contiene le impostazioni globali per la configurazione automatica delle reti cablate.</span><span class="sxs-lookup"><span data-stu-id="5c5cc-118">Contains the global settings for the automatic configuration of wired networks.</span></span> <br/>                                                                                          |
| [<span data-ttu-id="5c5cc-119">**nome**</span><span class="sxs-lookup"><span data-stu-id="5c5cc-119">**name**</span></span>](lan-policyschema-name-lanpolicy-element.md)                           | [<span data-ttu-id="5c5cc-120">**nameType**</span><span class="sxs-lookup"><span data-stu-id="5c5cc-120">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="5c5cc-121">Contiene il nome di un criterio LAN cablata.</span><span class="sxs-lookup"><span data-stu-id="5c5cc-121">Contains the name of a wired LAN policy.</span></span> <br/>                                                                                                                                 |
| [<span data-ttu-id="5c5cc-122">**profileList**</span><span class="sxs-lookup"><span data-stu-id="5c5cc-122">**profileList**</span></span>](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | <span data-ttu-id="5c5cc-123">Contiene un elenco di profili da applicare a livello di dominio o di computer.</span><span class="sxs-lookup"><span data-stu-id="5c5cc-123">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                                                                |



## <a name="remarks"></a><span data-ttu-id="5c5cc-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c5cc-124">Remarks</span></span>

<span data-ttu-id="5c5cc-125">Per visualizzare l'elenco di elementi figlio in una struttura ad albero, vedere [ \_ elementi dello schema del criterio LAN](lan-policyschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="5c5cc-125">To view the list of child elements in a tree-like structure, see [LAN\_policy Schema Elements](lan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c5cc-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c5cc-126">Requirements</span></span>



| <span data-ttu-id="5c5cc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c5cc-127">Requirement</span></span> | <span data-ttu-id="5c5cc-128">Valore</span><span class="sxs-lookup"><span data-stu-id="5c5cc-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c5cc-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c5cc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5c5cc-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c5cc-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c5cc-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c5cc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5c5cc-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c5cc-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




