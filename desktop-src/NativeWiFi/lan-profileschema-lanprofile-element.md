---
description: Contiene un profilo di rete cablata.
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: Elemento LANProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 58ad88c9f975455bdd2d77a0ef8ee028d9027d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232430"
---
# <a name="lanprofile-element"></a><span data-ttu-id="67d50-103">Elemento LANProfile</span><span class="sxs-lookup"><span data-stu-id="67d50-103">LANProfile Element</span></span>

<span data-ttu-id="67d50-104">L'elemento LANProfile contiene un profilo di rete cablata.</span><span class="sxs-lookup"><span data-stu-id="67d50-104">The LANProfile element contains a wired network profile.</span></span> <span data-ttu-id="67d50-105">Questo elemento è l'elemento radice univoco per un profilo di rete cablata.</span><span class="sxs-lookup"><span data-stu-id="67d50-105">This element is the unique root element for a wired network profile.</span></span>

<span data-ttu-id="67d50-106">Lo spazio dei nomi di destinazione per l'elemento LANProfile è `https://www.microsoft.com/networking/LAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="67d50-106">The target namespace for the LANProfile element is `https://www.microsoft.com/networking/LAN/profile/v1`.</span></span>

``` syntax
<xs:element name="LANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="MSM">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="security">
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="OneXEnforced"
                                        type="boolean"
                                     />
                                    <xs:element name="OneXEnabled"
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
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
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

## <a name="child-elements"></a><span data-ttu-id="67d50-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="67d50-107">Child elements</span></span>



| <span data-ttu-id="67d50-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="67d50-108">Element</span></span>                                                                 | <span data-ttu-id="67d50-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="67d50-109">Type</span></span>    | <span data-ttu-id="67d50-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67d50-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67d50-111">**MSM**</span><span class="sxs-lookup"><span data-stu-id="67d50-111">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)                 |         | <span data-ttu-id="67d50-112">Contiene le impostazioni CSM (media-Specific Module).</span><span class="sxs-lookup"><span data-stu-id="67d50-112">Contains media-specific module (MSM) settings.</span></span> <br/>                                                                               |
| [<span data-ttu-id="67d50-113">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="67d50-113">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="67d50-114">boolean</span><span class="sxs-lookup"><span data-stu-id="67d50-114">boolean</span></span> | <span data-ttu-id="67d50-115">Specifica se il servizio di configurazione automatica per reti cablate tenterà l'autenticazione della porta tramite 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="67d50-115">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="67d50-116">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="67d50-116">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="67d50-117">boolean</span><span class="sxs-lookup"><span data-stu-id="67d50-117">boolean</span></span> | <span data-ttu-id="67d50-118">Specifica se il servizio di configurazione automatica per reti cablate richiede l'utilizzo di 802.1 X per l'autenticazione della porta.</span><span class="sxs-lookup"><span data-stu-id="67d50-118">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="67d50-119">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="67d50-119">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="67d50-120">Contiene le impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="67d50-120">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="67d50-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="67d50-121">Remarks</span></span>

<span data-ttu-id="67d50-122">Per visualizzare l'elenco di elementi figlio in una struttura simile a un albero, [vedere \_ elementi dello schema del profilo LAN](lan-profileschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="67d50-122">To view the list of child elements in a tree-like structure, see [LAN\_profile Schema Elements](lan-profileschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67d50-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67d50-123">Requirements</span></span>



| <span data-ttu-id="67d50-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="67d50-124">Requirement</span></span> | <span data-ttu-id="67d50-125">Valore</span><span class="sxs-lookup"><span data-stu-id="67d50-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="67d50-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67d50-126">Minimum supported client</span></span><br/> | <span data-ttu-id="67d50-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67d50-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="67d50-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67d50-128">Minimum supported server</span></span><br/> | <span data-ttu-id="67d50-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="67d50-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




