---
description: Caratteristiche di gestione di un dispositivo USB.
ms.assetid: c0589346-7683-49c6-bd34-5ee38d71d00e
title: CIM_USBDevice classe (gestione Hyper-V)
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
ms.openlocfilehash: 3766d6c2fdc46b36350e9259e0e988f3a276cee6376d02de349abbe83bf8031b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427731"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a>CIM_USBDevice classe (gestione Hyper-V)

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

La **classe CIM \_ USBDevice** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe CIM \_ USBDevice** include questi metodi.



| Metodo                                               | Descrizione                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [**GetDescriptor**](cim-usbdevice-getdescriptor.md) | Recupera un descrittore di dispositivo USB.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe CIM \_ USBDevice** ha queste proprietà.

<dl> <dt>

**ClassCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bDeviceClass")
</dt> </dl>

Codice della classe USB.

</dd> <dt>

**CommandTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intervallo di timeout configurabile dalle applicazioni di gestione che supportano il reindirizzamento USB. Quando il servizio di reindirizzamento reindirizza un comando del dispositivo USB a un dispositivo remoto e il dispositivo remoto non risponde prima dell'intervallo di timeout, il servizio di reindirizzamento emulerà un evento di espulsione dei supporti. Inoltre, il servizio può provare nuovamente il comando o provare a ristabilire la connessione al dispositivo remoto.

</dd> <dt>

**CurrentAlternateSettings**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentConfigValue**")
</dt> </dl>

Matrice contenente le impostazioni alternative per ogni interfaccia nella configurazione corrente del dispositivo.

</dd> <dt>

**CurrentConfigValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentAlternateSettings**")
</dt> </dl>

Configurazione attualmente selezionata per il dispositivo. Se questo valore è zero, il dispositivo non è configurato.

</dd> <dt>

**DeviceReleaseNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bcdDevice")
</dt> </dl>

Numero di versione del dispositivo in formato BCD.

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| iManufacturer")
</dt> </dl>

Stringa del produttore del dispositivo.

</dd> <dt>

**MaxPacketSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bMaxPacketSize")
</dt> </dl>

Dimensione massima del pacchetto per l'endpoint USB zero.

</dd> <dt>

**NumberOfConfigs**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bNumConfigurations")
</dt> </dl>

Numero di configurazioni del dispositivo definite per il dispositivo.

</dd> <dt>

**Prodotto**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| iProduct")
</dt> </dl>

Stringa del prodotto del dispositivo.

</dd> <dt>

**ProductID**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| idProduct")
</dt> </dl>

ID prodotto assegnato al dispositivo dal produttore.

</dd> <dt>

**ProtocolCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bDeviceProtocol")
</dt> </dl>

Codice del protocollo USB.

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| iSerialNumber")
</dt> </dl>

Numero di serie del dispositivo.

</dd> <dt>

**SubclassCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bDeviceSubClass")
</dt> </dl>

Codice della sottoclasse USB.

</dd> <dt>

**USBVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione USB più recente supportata dal dispositivo USB. La proprietà è espressa come decimale a codice binario (BCD) che contiene un separatore decimale compreso tra la seconda e la terza cifra. Ad esempio, il valore 0x201 indica che è supportata la versione 2.01.

</dd> <dt>

**USBVersionInBCD**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| bcdUSB")
</dt> </dl>

Numero di specifica USB conforme al dispositivo. Questa proprietà è formattata con il formato BCD.

</dd> <dt>

**VendorID**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF \| Standard Device Descriptor \| idVendor")
</dt> </dl>

ID del fornitore assegnato al dispositivo dal USB.org.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

