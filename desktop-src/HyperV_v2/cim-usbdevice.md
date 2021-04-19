---
description: Caratteristiche di gestione di un dispositivo USB.
ms.assetid: c0589346-7683-49c6-bd34-5ee38d71d00e
title: Classe CIM_USBDevice (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.USBVersion
- CIM_USBDevice.ClassCode
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.USBVersionInBCD
- CIM_USBDevice.MaxPacketSize
- CIM_USBDevice.VendorID
- CIM_USBDevice.ProductID
- CIM_USBDevice.DeviceReleaseNumber
- CIM_USBDevice.Manufacturer
- CIM_USBDevice.Product
- CIM_USBDevice.SerialNumber
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CommandTimeout
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4b43c57d69f0f9eb92293aa8fa1ff1aa1ebe96c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310566"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a>Classe CIM_USBDevice (gestione Hyper-V)

Caratteristiche di gestione di un dispositivo USB.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::USB")]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   USBVersion;
  uint8    ClassCode;
  uint8    SubclassCode;
  uint8    ProtocolCode;
  uint16   USBVersionInBCD;
  uint8    MaxPacketSize;
  uint16   VendorID;
  uint16   ProductID;
  uint16   DeviceReleaseNumber;
  string   Manufacturer;
  string   Product;
  string   SerialNumber;
  uint8    NumberOfConfigs;
  uint8    CurrentConfigValue;
  uint8    CurrentAlternateSettings[];
  datetime CommandTimeout;
};
```

## <a name="members"></a>Members

La classe **CIM \_ usbdevice** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **CIM \_ usbdevice** presenta questi metodi.



| Metodo                                               | Descrizione                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [**GetDescriptor**](cim-usbdevice-getdescriptor.md) | Recupera un descrittore di dispositivo USB.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **CIM \_ usbdevice** dispone di queste proprietà.

<dl> <dt>

**ClassCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bDeviceClass")
</dt> </dl>

Codice della classe USB.

</dd> <dt>

**CommandTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intervallo di timeout configurabile dalle applicazioni di gestione che supportano il reindirizzamento USB. Quando il servizio di reindirizzamento reindirizza un comando del dispositivo USB a un dispositivo remoto e il dispositivo remoto non risponde prima dell'intervallo di timeout, il servizio di reindirizzamento emula un evento di espulsione del supporto. Il servizio può inoltre provare di nuovo a eseguire il comando o di ristabilire la connessione al dispositivo remoto.

</dd> <dt>

**CurrentAlternateSettings**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ usbdevice**.**CurrentConfigValue**")
</dt> </dl>

Matrice che contiene le impostazioni alternative per ogni interfaccia nella configurazione corrente del dispositivo.

</dd> <dt>

**CurrentConfigValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ usbdevice**.**CurrentAlternateSettings**")
</dt> </dl>

Configurazione attualmente selezionata per il dispositivo. Se questo valore è zero, il dispositivo non è configurato.

</dd> <dt>

**DeviceReleaseNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bcdDevice")
</dt> </dl>

Numero di rilascio del dispositivo in formato BCD.

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| iManufacturer")
</dt> </dl>

Stringa del produttore del dispositivo.

</dd> <dt>

**MaxPacketSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bMaxPacketSize")
</dt> </dl>

Dimensioni massime del pacchetto per l'endpoint USB zero.

</dd> <dt>

**NumberOfConfigs**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bNumConfigurations")
</dt> </dl>

Il numero di configurazioni del dispositivo definite per il dispositivo.

</dd> <dt>

**Prodotto**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| IProduct")
</dt> </dl>

Stringa di prodotto del dispositivo.

</dd> <dt>

**ProductID**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| idProduct")
</dt> </dl>

ID prodotto assegnato al dispositivo dal produttore.

</dd> <dt>

**ProtocolCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bDeviceProtocol")
</dt> </dl>

Codice del protocollo USB.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| iSerialNumber")
</dt> </dl>

Numero di serie del dispositivo.

</dd> <dt>

**SubclassCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bDeviceSubClass")
</dt> </dl>

Codice della sottoclasse USB.

</dd> <dt>

**USBVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione USB più recente supportata dal dispositivo USB. La proprietà è espressa come un valore decimale (BCD) con codifica binaria che contiene un separatore decimale compreso tra il secondo e il terzo. Ad esempio, il valore 0x201 indica che la versione 2,01 è supportata.

</dd> <dt>

**USBVersionInBCD**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bcdUSB")
</dt> </dl>

Il numero di specifica USB a cui è conforme il dispositivo. Questa proprietà è formattata con il formato BCD.

</dd> <dt>

**VendorID**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| idVendor")
</dt> </dl>

ID del fornitore assegnato al dispositivo da USB.org.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

