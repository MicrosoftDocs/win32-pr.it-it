---
title: Enumerazione SoHAttributeType (NapProtocol.h)
description: Specifica il tipo di attributo archiviato nell'oggetto type-length-value (TLV) dell'attributo.
ms.assetid: ba725bf1-1d0a-4489-b912-3e761557d772
keywords:
- Enumerazione SoHAttributeType NAP
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
ms.openlocfilehash: 1c3fabf3a8911274b912f3762dd07d0c64fc4111d22e372d1962a92221f1d068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939058"
---
# <a name="sohattributetype-enumeration"></a>Enumerazione SoHAttributeType

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**L'enumerazione SoHAttributeType** specifica il tipo di attributo archiviato nell'oggetto TLV (Type-Length-Value) dell'attributo.

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

Specifica l'ora dell'ultimo tipo di attributo di aggiornamento.

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

Specifica il tipo di attributo della versione software.

</dd> <dt>

<span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**
</dt> <dd>

Specifica il tipo di attributo product name.

</dd> <dt>

<span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**
</dt> <dd>

Specifica il tipo di attributo di stato della classe di integrità.

</dd> <dt>

<span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**
</dt> <dd>

Specifica l'ora di generazione del tipo di attributo Statement of Health.

</dd> <dt>

<span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**
</dt> <dd>

Specifica il tipo di attributo del codice di errore.

</dd> <dt>

<span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**
</dt> <dd>

Specifica il tipo di attributo della categoria di errori.

</dd> <dt>

<span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**
</dt> <dd>

Specifica il tipo di attributo del server di correzione IPv6.

</dd> <dt>

<span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**
</dt> <dd>

Specifica il tipo di attributo dello stato di isolamento esteso.

</dd> </dl>

## <a name="remarks"></a>Commenti

La [**struttura SoHAttributeValue**](sohattributevalue-union.md) definisce i valori degli attributi che corrispondono a ogni tipo di attributo.

Questi tipi di attributi vengono utilizzati dal sistema di Protezione accesso alla rete:

-   sohAttributeTypeSystemHealthId
-   sohAttributeTypeIpv4FixupServers
-   sohAttributeTypeIpv6FixupServers
-   sohAttributeTypeComplianceResultCodes
-   sohAttributeTypeFailureCategory

Il resto dei tipi è destinato solo a guidare l'utilizzo da parte di SHAs e SHV.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SoHAttributeValue**](sohattributevalue-union.md)
</dt> <dt>

[**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)
</dt> <dt>

[**Soh**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





