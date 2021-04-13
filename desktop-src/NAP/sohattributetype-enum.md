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
# <a name="sohattributetype-enumeration"></a>Enumerazione SoHAttributeType

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'enumerazione **SoHAttributeType** specifica il tipo di attributo archiviato nell'oggetto Type-Length-Value (TLV) dell'attributo.

## <a name="syntax"></a>Sintassi


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



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohAttributeTypeSystemHealthId**
</dt> <dd>

Specifica il tipo di attributo ID integrità sistema.

</dd> <dt>

<span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**
</dt> <dd>

Specifica il tipo di attributo del server di correzione IPv4.

</dd> <dt>

<span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohAttributeTypeComplianceResultCodes**
</dt> <dd>

Specifica il tipo di attributo del codice del risultato di conformità.

</dd> <dt>

<span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohAttributeTypeTimeOfLastUpdate**
</dt> <dd>

Specifica l'ora dell'ultimo tipo di attributo Update.

</dd> <dt>

<span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohAttributeTypeClientId**
</dt> <dd>

Specifica il tipo di attributo ID client.

</dd> <dt>

<span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohAttributeTypeVendorSpecific**
</dt> <dd>

Specifica il tipo di attributo specifico del fornitore.

</dd> <dt>

<span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohAttributeTypeHealthClass**
</dt> <dd>

Specifica il tipo di attributo della classe di integrità.

</dd> <dt>

<span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohAttributeTypeSoftwareVersion**
</dt> <dd>

Specifica il tipo di attributo della versione del software.

</dd> <dt>

<span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**
</dt> <dd>

Specifica il tipo di attributo Product Name.

</dd> <dt>

<span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**
</dt> <dd>

Specifica il tipo di attributo status della classe Health.

</dd> <dt>

<span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**
</dt> <dd>

Specifica la data e l'ora di generazione dell'istruzione del tipo di attributo Health.

</dd> <dt>

<span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**
</dt> <dd>

Specifica il tipo di attributo del codice di errore.

</dd> <dt>

<span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**
</dt> <dd>

Specifica il tipo di attributo della categoria di errore.

</dd> <dt>

<span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**
</dt> <dd>

Specifica il tipo di attributo del server di correzione IPv6.

</dd> <dt>

<span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**
</dt> <dd>

Specifica il tipo di attributo di stato di isolamento esteso.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura [**SoHAttributeValue**](sohattributevalue-union.md) definisce i valori dell'attributo che corrispondono a ogni tipo di attributo.

Questi tipi di attributo vengono utilizzati dal sistema NAP:

-   sohAttributeTypeSystemHealthId
-   sohAttributeTypeIpv4FixupServers
-   sohAttributeTypeIpv6FixupServers
-   sohAttributeTypeComplianceResultCodes
-   sohAttributeTypeFailureCategory

Il resto dei tipi viene progettato solo per guidare l'utilizzo di SHAs e SHV.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SoHAttributeValue**](sohattributevalue-union.md)
</dt> <dt>

[**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)
</dt> <dt>

[**Rapporto**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





