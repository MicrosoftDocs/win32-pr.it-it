---
title: Enumerazione SoHAttributeType (NapProtocol. h)
description: Specifica il tipo di attributo archiviato nell'oggetto del tipo di attributo-length-value (TLV).
ms.assetid: ba725bf1-1d0a-4489-b912-3e761557d772
keywords:
- SoHAttributeType enumerazione NAP
topic_type:
- apiref
api_name:
- SoHAttributeType
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db164bbedf2267aaa5941a21a56ccfd53e1e1646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340992"
---
# <a name="sohattributetype-enumeration"></a><span data-ttu-id="84ab3-104">Enumerazione SoHAttributeType</span><span class="sxs-lookup"><span data-stu-id="84ab3-104">SoHAttributeType enumeration</span></span>

> [!Note]  
> <span data-ttu-id="84ab3-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="84ab3-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="84ab3-106">L'enumerazione **SoHAttributeType** specifica il tipo di attributo archiviato nell'oggetto Type-Length-Value (TLV) dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="84ab3-106">The **SoHAttributeType** enumeration specifies the type of attribute stored in the attribute type-length-value (TLV) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="84ab3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84ab3-107">Syntax</span></span>


```C++
typedef enum tagSoHAttributeType { 
  sohAttributeTypeSystemHealthId          = 2,
  sohAttributeTypeIpv4FixupServers        = 3,
  sohAttributeTypeComplianceResultCodes   = 4,
  sohAttributeTypeTimeOfLastUpdate        = 5,
  sohAttributeTypeClientId                = 6,
  sohAttributeTypeVendorSpecific          = 7,
  sohAttributeTypeHealthClass             = 8,
  sohAttributeTypeSoftwareVersion         = 9,
  sohAttributeTypeProductName             = 10,
  sohAttributeTypeHealthClassStatus       = 11,
  sohAttributeTypeSoHGenerationTime       = 12,
  sohAttributeTypeErrorCodes              = 13,
  sohAttributeTypeFailureCategory         = 14,
  sohAttributeTypeIpv6FixupServers        = 15,
  sohAttributeTypeExtendedIsolationState  = 16
} SoHAttributeType;
```



## <a name="constants"></a><span data-ttu-id="84ab3-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="84ab3-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="84ab3-109"><span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohAttributeTypeSystemHealthId**</span><span class="sxs-lookup"><span data-stu-id="84ab3-109"><span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohAttributeTypeSystemHealthId**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-110">Specifica il tipo di attributo ID integrità sistema.</span><span class="sxs-lookup"><span data-stu-id="84ab3-110">Specifies the system health ID attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-111"><span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**</span><span class="sxs-lookup"><span data-stu-id="84ab3-111"><span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-112">Specifica il tipo di attributo del server di correzione IPv4.</span><span class="sxs-lookup"><span data-stu-id="84ab3-112">Specifies the IPv4 fix-up server attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-113"><span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohAttributeTypeComplianceResultCodes**</span><span class="sxs-lookup"><span data-stu-id="84ab3-113"><span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohAttributeTypeComplianceResultCodes**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-114">Specifica il tipo di attributo del codice del risultato di conformità.</span><span class="sxs-lookup"><span data-stu-id="84ab3-114">Specifies the compliance result code attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-115"><span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohAttributeTypeTimeOfLastUpdate**</span><span class="sxs-lookup"><span data-stu-id="84ab3-115"><span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohAttributeTypeTimeOfLastUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-116">Specifica l'ora dell'ultimo tipo di attributo Update.</span><span class="sxs-lookup"><span data-stu-id="84ab3-116">Specifies the time of the last update attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-117"><span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohAttributeTypeClientId**</span><span class="sxs-lookup"><span data-stu-id="84ab3-117"><span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohAttributeTypeClientId**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-118">Specifica il tipo di attributo ID client.</span><span class="sxs-lookup"><span data-stu-id="84ab3-118">Specifies the client ID attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-119"><span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohAttributeTypeVendorSpecific**</span><span class="sxs-lookup"><span data-stu-id="84ab3-119"><span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohAttributeTypeVendorSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-120">Specifica il tipo di attributo specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="84ab3-120">Specifies the vendor-specific attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-121"><span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohAttributeTypeHealthClass**</span><span class="sxs-lookup"><span data-stu-id="84ab3-121"><span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohAttributeTypeHealthClass**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-122">Specifica il tipo di attributo della classe di integrità.</span><span class="sxs-lookup"><span data-stu-id="84ab3-122">Specifies the health class attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-123"><span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohAttributeTypeSoftwareVersion**</span><span class="sxs-lookup"><span data-stu-id="84ab3-123"><span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohAttributeTypeSoftwareVersion**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-124">Specifica il tipo di attributo della versione del software.</span><span class="sxs-lookup"><span data-stu-id="84ab3-124">Specifies the software version attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-125"><span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**</span><span class="sxs-lookup"><span data-stu-id="84ab3-125"><span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-126">Specifica il tipo di attributo Product Name.</span><span class="sxs-lookup"><span data-stu-id="84ab3-126">Specifies the product name attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-127"><span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**</span><span class="sxs-lookup"><span data-stu-id="84ab3-127"><span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-128">Specifica il tipo di attributo status della classe Health.</span><span class="sxs-lookup"><span data-stu-id="84ab3-128">Specifies the health class status attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-129"><span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**</span><span class="sxs-lookup"><span data-stu-id="84ab3-129"><span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-130">Specifica la data e l'ora di generazione dell'istruzione del tipo di attributo Health.</span><span class="sxs-lookup"><span data-stu-id="84ab3-130">Specifies the generation time of the Statement of Health attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-131"><span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**</span><span class="sxs-lookup"><span data-stu-id="84ab3-131"><span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-132">Specifica il tipo di attributo del codice di errore.</span><span class="sxs-lookup"><span data-stu-id="84ab3-132">Specifies the error code attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-133"><span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**</span><span class="sxs-lookup"><span data-stu-id="84ab3-133"><span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-134">Specifica il tipo di attributo della categoria di errore.</span><span class="sxs-lookup"><span data-stu-id="84ab3-134">Specifies the failure category attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-135"><span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**</span><span class="sxs-lookup"><span data-stu-id="84ab3-135"><span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-136">Specifica il tipo di attributo del server di correzione IPv6.</span><span class="sxs-lookup"><span data-stu-id="84ab3-136">Specifies the IPv6 fix-up server attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="84ab3-137"><span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**</span><span class="sxs-lookup"><span data-stu-id="84ab3-137"><span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**</span></span>
</dt> <dd>

<span data-ttu-id="84ab3-138">Specifica il tipo di attributo di stato di isolamento esteso.</span><span class="sxs-lookup"><span data-stu-id="84ab3-138">Specifies the extended isolation state attribute type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84ab3-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="84ab3-139">Remarks</span></span>

<span data-ttu-id="84ab3-140">La struttura [**SoHAttributeValue**](sohattributevalue-union.md) definisce i valori dell'attributo che corrispondono a ogni tipo di attributo.</span><span class="sxs-lookup"><span data-stu-id="84ab3-140">The [**SoHAttributeValue**](sohattributevalue-union.md) structure defines the attribute values that correspond to each attribute type.</span></span>

<span data-ttu-id="84ab3-141">Questi tipi di attributo vengono utilizzati dal sistema NAP:</span><span class="sxs-lookup"><span data-stu-id="84ab3-141">These attribute types are consumed by the NAP system:</span></span>

-   <span data-ttu-id="84ab3-142">sohAttributeTypeSystemHealthId</span><span class="sxs-lookup"><span data-stu-id="84ab3-142">sohAttributeTypeSystemHealthId</span></span>
-   <span data-ttu-id="84ab3-143">sohAttributeTypeIpv4FixupServers</span><span class="sxs-lookup"><span data-stu-id="84ab3-143">sohAttributeTypeIpv4FixupServers</span></span>
-   <span data-ttu-id="84ab3-144">sohAttributeTypeIpv6FixupServers</span><span class="sxs-lookup"><span data-stu-id="84ab3-144">sohAttributeTypeIpv6FixupServers</span></span>
-   <span data-ttu-id="84ab3-145">sohAttributeTypeComplianceResultCodes</span><span class="sxs-lookup"><span data-stu-id="84ab3-145">sohAttributeTypeComplianceResultCodes</span></span>
-   <span data-ttu-id="84ab3-146">sohAttributeTypeFailureCategory</span><span class="sxs-lookup"><span data-stu-id="84ab3-146">sohAttributeTypeFailureCategory</span></span>

<span data-ttu-id="84ab3-147">Il resto dei tipi viene progettato solo per guidare l'utilizzo di SHAs e SHV.</span><span class="sxs-lookup"><span data-stu-id="84ab3-147">The rest of the types are only intended to guide the usage by SHAs and SHVs.</span></span>

## <a name="requirements"></a><span data-ttu-id="84ab3-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84ab3-148">Requirements</span></span>



| <span data-ttu-id="84ab3-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="84ab3-149">Requirement</span></span> | <span data-ttu-id="84ab3-150">Valore</span><span class="sxs-lookup"><span data-stu-id="84ab3-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="84ab3-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84ab3-151">Minimum supported client</span></span><br/> | <span data-ttu-id="84ab3-152">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84ab3-152">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="84ab3-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84ab3-153">Minimum supported server</span></span><br/> | <span data-ttu-id="84ab3-154">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84ab3-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="84ab3-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84ab3-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="84ab3-156"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="84ab3-156"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="84ab3-157">IDL</span><span class="sxs-lookup"><span data-stu-id="84ab3-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84ab3-158"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84ab3-158"><dt>NapProtocol.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84ab3-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84ab3-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84ab3-160">**SoHAttributeValue**</span><span class="sxs-lookup"><span data-stu-id="84ab3-160">**SoHAttributeValue**</span></span>](sohattributevalue-union.md)
</dt> <dt>

[<span data-ttu-id="84ab3-161">**SoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="84ab3-161">**SoHAttribute**</span></span>](/windows/win32/api/naptypes/ns-naptypes-sohattribute)
</dt> <dt>

[<span data-ttu-id="84ab3-162">**Rapporto**</span><span class="sxs-lookup"><span data-stu-id="84ab3-162">**SoH**</span></span>](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> <dt>

[<span data-ttu-id="84ab3-163">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="84ab3-163">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> <dt>

[<span data-ttu-id="84ab3-164">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="84ab3-164">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





