---
title: Unione SoHAttributeValue (NapProtocol. h)
description: Definisce il contenuto del membro del tipo in una struttura SoHAttribute.
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- NAP Unione SoHAttributeValue
topic_type:
- apiref
api_name:
- SoHAttributeValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36660e4e360ff0df31bb3a76d06c50e5d366c894
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478442"
---
# <a name="sohattributevalue-union"></a>Unione SoHAttributeValue

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'Unione **SoHAttributeValue** definisce il contenuto del membro del **tipo** in una struttura [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) . La struttura dell'Unione **SoHAttributeValue** è determinata dall'oggetto [**SoHAttributeType**](sohattributetype-enum.md) specificato nel membro del **tipo** della struttura [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .

## <a name="syntax"></a>Sintassi


```C++
typedef union tagSoHAttributeValue {
  SystemHealthEntityId     idVal;
  struct tagIpv4Addresses {
    UINT16      count;
    Ipv4Address *addresses;
  } v4AddressesVal;
  struct tagIpv6Addresses {
    UINT16      count;
    Ipv6Address *addresses;
  } v6AddressesVal;
  ResultCodes              codesVal;
  FILETIME                 dateTimeVal;
  struct tagVendorSpecific {
    UINT32 vendorId;
    UINT16 size;
    BYTE   *vendorSpecificData;
  } vendorSpecificVal;
  UINT8                    uint8Val;
  struct tagOctetString {
    UINT16 size;
    BYTE   *data;
  } octetStringVal;
} SoHAttributeValue;
```



## <a name="members"></a>Members

<dl> <dt>

**idVal**
</dt> <dd>

**caso (sohAttributeTypeSystemHealthId)**

[SystemHealthEntityId](nap-datatypes.md) univoco che contiene l'ID dell'agente integrità sistema (SHA) o del servizio di convalida dell'integrità di sistema che ha costruito questo pacchetto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

**v4AddressesVal**
</dt> <dd>

**caso (sohAttributeTypeIpv4FixupServers)**

Indirizzi IPv4 dei server di correzione utilizzati dal sistema NAP.

<dl> <dt>

**count**
</dt> <dd>

Numero di indirizzi IPv4 nel membro degli **indirizzi** compresi nell'intervallo da 1 a [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).

</dd> <dt>

**indirizzi**
</dt> <dd>

Matrice di strutture [**IndirizzoIPv4**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) che contengono gli indirizzi IPv4.

</dd> </dl> </dd> <dt>

**v6AddressesVal**
</dt> <dd>

**caso (sohAttributeTypeIpv6FixupServers)**

Indirizzi IPv6 dei server di correzione utilizzati dal sistema NAP.

<dl> <dt>

**count**
</dt> <dd>

Numero di indirizzi IPv4 nel membro degli **indirizzi** compresi nell'intervallo da 1 a [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).

</dd> <dt>

**indirizzi**
</dt> <dd>

Matrice di strutture [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) che contengono gli indirizzi IPv4.

</dd> </dl> </dd> <dt>

**codesVal**
</dt> <dd>

**Case (sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**

Struttura [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) che contiene i codici di risultato della conformità definiti dall'applicazione delle costanti di [**errore**](nap-error-constants.md)client o NAP. Un pacchetto di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) deve contenere questo TLV o il **sohAttributeTypeFailureCategory** TLV.

</dd> <dt>

**dateTimeVal**
</dt> <dd>

**Case (sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**

Struttura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) che contiene l'ora dell'ultimo aggiornamento del rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) o del tempo di generazione del rapporto di **integrità** .

</dd> <dt>

**vendorSpecificVal**
</dt> <dd>

**caso (sohAttributeTypeVendorSpecific)**

Dati specifici dell'applicazione definiti dal fornitore.

<dl> <dt>

**vendorId**
</dt> <dd>

Identificatore a 4 byte che definisce l'ID della coppia SHA/convalida. I primi 3 byte sono il codice SMI assegnato dall'IETF del fornitore e l'ultimo byte identifica il componente stesso. Quando si implementa un SHA o un servizio di convalida dell'integrità di sistema, non usare i valori ID assegnati ai componenti interni di integrità del sistema Microsoft nelle [**costanti del fornitore NAP**](nap-vendor-constants.md).

</dd> <dt>

**size**
</dt> <dd>

Dimensione, in byte, dei dati del fornitore nell'intervallo compreso tra 0 e ([**maxSoHAttributeSize**](nap-type-constants.md) -4).

</dd> <dt>

**vendorSpecificData**
</dt> <dd>

Puntatore ai dati specifici del fornitore nell'ordine dei byte di rete.

</dd> </dl> </dd> <dt>

**uint8Val**
</dt> <dd>

**Case (sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory, sohAttributeTypeExtendedIsolationState)**

La classe di integrità, la categoria di errore o lo stato di isolamento esteso di un componente NAP come valore [**HealthClassValue**](healthclassvalue-enum.md) o [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) o come struttura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) .

</dd> <dt>

**octetStringVal**
</dt> <dd>

**default**

I valori degli attributi seguenti sono stringhe ottetto:

-   sohAttributeTypeSoftwareVersion
-   sohAttributeTypeClientId
-   sohAttributeTypeProductName
-   sohAttributeTypeHealthClassStatus

Per la compatibilità con le edizioni, tutti gli attributi non riconosciuti vengono restituiti come stringhe ottetto. **i dati** devono essere in ordine byte di rete.

<dl> <dt>

**size**
</dt> <dd>

Dimensione, in byte, dei **dati** nell'intervallo compreso tra 0 e [**maxSoHAttributeSize**](nap-type-constants.md).

</dd> <dt>

**data**
</dt> <dd>

Puntatore al valore della stringa ottetto.

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a>Layout dati effettivo

A causa della natura dell'ambiente di pubblicazione dell'SDK, le unioni non sono chiaramente rappresentate nei blocchi di sintassi. Di seguito è illustrata la sintassi effettiva del file di intestazione NapProtocol. h.


```C++
#include <windows.h>

typedef [switch_type(SoHAttributeType)] 
   union tagSoHAttributeValue
   {
      [case(sohAttributeTypeSystemHealthId)]
         SystemHealthEntityId idVal;
   
      [case(sohAttributeTypeIpv4FixupServers)]
         struct tagIpv4Addresses
         {
            [range(1, maxIpv4CountPerSoHAttribute)] 
               UINT16 count;
            [size_is(count)] Ipv4Address* addresses;
         } v4AddressesVal;

      [case(sohAttributeTypeIpv6FixupServers)]
         struct tagIpv6Addresses
         {
            [range(1, maxIpv6CountPerSoHAttribute)]
               UINT16 count;
            [size_is(count)] Ipv6Address* addresses;
         } v6AddressesVal;

      [case(sohAttributeTypeComplianceResultCodes, 
            sohAttributeTypeErrorCodes)]
         ResultCodes codesVal;

      [case(sohAttributeTypeTimeOfLastUpdate, 
            sohAttributeTypeSoHGenerationTime)]
         FILETIME dateTimeVal;

      [case(sohAttributeTypeVendorSpecific)]
         struct tagVendorSpecific
         {
            UINT32 vendorId;
            [range(0, maxSoHAttributeSize - 4)] 
               UINT16 size;
            [size_is(size)] BYTE* vendorSpecificData;
         } vendorSpecificVal;

      [case(sohAttributeTypeHealthClass, 
            sohAttributeTypeFailureCategory,
            sohAttributeTypeExtendedIsolationState)]
         UINT8 uint8Val;

      [default]
         struct tagOctetString
         {
            [range(0, maxSoHAttributeSize)] UINT16 size;
            [size_is(size)] BYTE* data;
         } octetStringVal;

   } SoHAttributeValue;
};
```



## <a name="remarks"></a>Commenti

Questi tipi di attributo vengono utilizzati dal sistema NAP:

-   sohAttributeTypeSystemHealthId
-   sohAttributeTypeIpv4FixupServers
-   sohAttributeTypeIpv6FixupServers
-   sohAttributeTypeComplianceResultCodes
-   sohAttributeTypeFailureCategory

Gli altri [**SoHAttributeTypes**](sohattributetype-enum.md) sono intesi esclusivamente come linee guida descrittive per l'utilizzo da parte di Shas e SHV.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento NAP](nap-reference.md)
</dt> <dt>

[Strutture NAP](nap-structures.md)
</dt> </dl>

 

