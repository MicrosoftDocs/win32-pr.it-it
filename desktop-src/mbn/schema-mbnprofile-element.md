---
description: È l'elemento radice che identifica un profilo a banda larga mobile.
ms.assetid: 08302e7f-3024-439b-a2ad-a4ae9487b82b
title: Elemento MBNProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MBNProfile
api_type:
- Schema
ms.openlocfilehash: 7016d492a70192a7d6accdcb3aaa57a9c564960e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307538"
---
# <a name="mbnprofile-element"></a><span data-ttu-id="7e00c-103">Elemento MBNProfile</span><span class="sxs-lookup"><span data-stu-id="7e00c-103">MBNProfile Element</span></span>

<span data-ttu-id="7e00c-104">L'elemento **MBNProfile** è l'elemento radice che identifica un profilo a banda larga mobile.</span><span class="sxs-lookup"><span data-stu-id="7e00c-104">The **MBNProfile** element is the root element that identifies a Mobile Broadband profile.</span></span>

<span data-ttu-id="7e00c-105">Può essere presente un solo elemento di questo tipo per documento.</span><span class="sxs-lookup"><span data-stu-id="7e00c-105">There can only be one element of this type per document.</span></span>

``` syntax
<xs:element name="MBNProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="nameType"
             />
            <xs:element name="Description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="ICONFilePath"
                type="iconFileType"
                minOccurs="0"
             />
            <xs:element name="IsDefault"
                type="boolean"
             />
            <xs:element name="ProfileCreationType"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="token"
                    >
                        <xs:enumeration
                            value="UserProvisioned"
                         />
                        <xs:enumeration
                            value="AdminProvisioned"
                         />
                        <xs:enumeration
                            value="OperatorProvisioned"
                         />
                        <xs:enumeration
                            value="DeviceProvisioned"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="SubscriberID"
                type="subscriberIdType"
             />
            <xs:element name="SimIccID"
                type="simIccIDType"
                minOccurs="0"
             />
            <xs:element name="HomeProviderName"
                type="providerNameType"
                minOccurs="0"
             />
            <xs:element name="AutoConnectOnInternet"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="ConnectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="manual"
                         />
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="auto-home"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="Context"
                type="contextType"
                minOccurs="0"
             />
            <xs:element name="DataRoamingPartners"
                minOccurs="0"
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
```

## <a name="child-elements"></a><span data-ttu-id="7e00c-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="7e00c-106">Child elements</span></span>



| <span data-ttu-id="7e00c-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e00c-107">Element</span></span>                                                                          | <span data-ttu-id="7e00c-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e00c-108">Type</span></span>                                                           | <span data-ttu-id="7e00c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e00c-109">Description</span></span>                                               |
|----------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="7e00c-110">**AutoConnectOnInternet**</span><span class="sxs-lookup"><span data-stu-id="7e00c-110">**AutoConnectOnInternet**</span></span>](schema-autoconnectoninternet-mbnprofile-element.md) | <span data-ttu-id="7e00c-111">boolean</span><span class="sxs-lookup"><span data-stu-id="7e00c-111">boolean</span></span>                                                        | <span data-ttu-id="7e00c-112">Indica se il dispositivo si connetterà automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7e00c-112">Whether the device will automatically connect.</span></span><br/> |
| [<span data-ttu-id="7e00c-113">**ConnectionMode**</span><span class="sxs-lookup"><span data-stu-id="7e00c-113">**ConnectionMode**</span></span>](schema-connectionmode-mbnprofile-element.md)               |                                                                | <span data-ttu-id="7e00c-114">Impostazioni di connessione automatica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e00c-114">The device auto connection settings.</span></span><br/>           |
| [<span data-ttu-id="7e00c-115">**Context**</span><span class="sxs-lookup"><span data-stu-id="7e00c-115">**Context**</span></span>](schema-context-mbnprofile-element.md)                             | [<span data-ttu-id="7e00c-116">**contextType**</span><span class="sxs-lookup"><span data-stu-id="7e00c-116">**contextType**</span></span>](schema-contexttype-complextype.md)          | <span data-ttu-id="7e00c-117">Parametri di configurazione della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="7e00c-117">Data connection setup parameters.</span></span><br/>              |
| [<span data-ttu-id="7e00c-118">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="7e00c-118">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)     |                                                                | <span data-ttu-id="7e00c-119">Provider di rete preferiti per il roaming.</span><span class="sxs-lookup"><span data-stu-id="7e00c-119">Preferred network providers for roaming.</span></span><br/>       |
| [<span data-ttu-id="7e00c-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7e00c-120">**Description**</span></span>](schema-description-mbnprofile-element.md)                     | [<span data-ttu-id="7e00c-121">**nameType**</span><span class="sxs-lookup"><span data-stu-id="7e00c-121">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="7e00c-122">Descrizione del profilo.</span><span class="sxs-lookup"><span data-stu-id="7e00c-122">Description of the profile.</span></span><br/>                    |
| [<span data-ttu-id="7e00c-123">**HomeProviderName**</span><span class="sxs-lookup"><span data-stu-id="7e00c-123">**HomeProviderName**</span></span>](schema-homeprovidername-mbnprofile-element.md)           | [<span data-ttu-id="7e00c-124">**providerNameType**</span><span class="sxs-lookup"><span data-stu-id="7e00c-124">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="7e00c-125">Nome del provider home.</span><span class="sxs-lookup"><span data-stu-id="7e00c-125">Name of the home provider.</span></span><br/>                     |
| [<span data-ttu-id="7e00c-126">**ICONFilePath**</span><span class="sxs-lookup"><span data-stu-id="7e00c-126">**ICONFilePath**</span></span>](schema-iconfilepath-mbnprofile-element.md)                   | [<span data-ttu-id="7e00c-127">**iconFileType**</span><span class="sxs-lookup"><span data-stu-id="7e00c-127">**iconFileType**</span></span>](schema-iconfiletype-simpletype.md)         | <span data-ttu-id="7e00c-128">Percorso del file icona.</span><span class="sxs-lookup"><span data-stu-id="7e00c-128">Path to the icon file.</span></span><br/>                         |
| [<span data-ttu-id="7e00c-129">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="7e00c-129">**IsDefault**</span></span>](schema-isdefault-mbnprofile-element.md)                         | <span data-ttu-id="7e00c-130">boolean</span><span class="sxs-lookup"><span data-stu-id="7e00c-130">boolean</span></span>                                                        | <span data-ttu-id="7e00c-131">Indica se il profilo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7e00c-131">Whether the profile is the default.</span></span><br/>            |
| [<span data-ttu-id="7e00c-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7e00c-132">**Name**</span></span>](schema-name-mbnprofile-element.md)                                   | [<span data-ttu-id="7e00c-133">**nameType**</span><span class="sxs-lookup"><span data-stu-id="7e00c-133">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="7e00c-134">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="7e00c-134">Name of the profile.</span></span><br/>                           |
| [<span data-ttu-id="7e00c-135">**ProfileCreationType**</span><span class="sxs-lookup"><span data-stu-id="7e00c-135">**ProfileCreationType**</span></span>](schema-profilecreationtype-mbnprofile-element.md)     |                                                                | <span data-ttu-id="7e00c-136">Informazioni sull'autore del profilo.</span><span class="sxs-lookup"><span data-stu-id="7e00c-136">Information about the profile creator.</span></span><br/>         |
| [<span data-ttu-id="7e00c-137">**SimIccID**</span><span class="sxs-lookup"><span data-stu-id="7e00c-137">**SimIccID**</span></span>](schema-simiccid-mbnprofile-element.md)                           | [<span data-ttu-id="7e00c-138">**simIccIDType**</span><span class="sxs-lookup"><span data-stu-id="7e00c-138">**simIccIDType**</span></span>](schema-simiccidtype-simpletype.md)         | <span data-ttu-id="7e00c-139">Numero di identificazione della SIM per i dispositivi GSM.</span><span class="sxs-lookup"><span data-stu-id="7e00c-139">SIM identification number for GSM devices.</span></span><br/>     |
| [<span data-ttu-id="7e00c-140">**SubscriberID**</span><span class="sxs-lookup"><span data-stu-id="7e00c-140">**SubscriberID**</span></span>](schema-subscriberid-mbnprofile-element.md)                   | [<span data-ttu-id="7e00c-141">**subscriberIdType**</span><span class="sxs-lookup"><span data-stu-id="7e00c-141">**subscriberIdType**</span></span>](schema-subscriberidtype-simpletype.md) | <span data-ttu-id="7e00c-142">Identificatore univoco del profilo.</span><span class="sxs-lookup"><span data-stu-id="7e00c-142">Unique identifier of the profile.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="7e00c-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e00c-143">Requirements</span></span>



| <span data-ttu-id="7e00c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e00c-144">Requirement</span></span> | <span data-ttu-id="7e00c-145">Valore</span><span class="sxs-lookup"><span data-stu-id="7e00c-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="7e00c-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e00c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7e00c-147">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7e00c-147">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="7e00c-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e00c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7e00c-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7e00c-149">None supported</span></span><br/>                         |



 

 




