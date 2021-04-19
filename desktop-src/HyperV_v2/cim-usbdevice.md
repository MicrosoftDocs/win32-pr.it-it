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
# <a name="cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="b4fe1-103">Classe CIM_USBDevice (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="b4fe1-103">CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="b4fe1-104">Caratteristiche di gestione di un dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-104">The management characteristics of a USB device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4fe1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4fe1-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="b4fe1-106">Members</span><span class="sxs-lookup"><span data-stu-id="b4fe1-106">Members</span></span>

<span data-ttu-id="b4fe1-107">La classe **CIM \_ usbdevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b4fe1-107">The **CIM\_USBDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="b4fe1-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="b4fe1-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="b4fe1-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b4fe1-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b4fe1-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="b4fe1-110">Methods</span></span>

<span data-ttu-id="b4fe1-111">La classe **CIM \_ usbdevice** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-111">The **CIM\_USBDevice** class has these methods.</span></span>



| <span data-ttu-id="b4fe1-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="b4fe1-112">Method</span></span>                                               | <span data-ttu-id="b4fe1-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4fe1-113">Description</span></span>                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [<span data-ttu-id="b4fe1-114">**GetDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-114">**GetDescriptor**</span></span>](cim-usbdevice-getdescriptor.md) | <span data-ttu-id="b4fe1-115">Recupera un descrittore di dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-115">Retrieves a USB device descriptor.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b4fe1-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b4fe1-116">Properties</span></span>

<span data-ttu-id="b4fe1-117">La classe **CIM \_ usbdevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-117">The **CIM\_USBDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4fe1-118">**ClassCode**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-118">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-119">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-121">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bDeviceClass")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceClass")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-122">Codice della classe USB.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-122">The USB class code.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-123">**CommandTimeout**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-123">**CommandTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-124">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-126">Intervallo di timeout configurabile dalle applicazioni di gestione che supportano il reindirizzamento USB.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-126">A timeout interval that is configurable by management applications that support USB redirection.</span></span> <span data-ttu-id="b4fe1-127">Quando il servizio di reindirizzamento reindirizza un comando del dispositivo USB a un dispositivo remoto e il dispositivo remoto non risponde prima dell'intervallo di timeout, il servizio di reindirizzamento emula un evento di espulsione del supporto.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-127">When the redirection service redirects a USB device command to a remote device, and the remote device does not respond before timeout interval, the redirection service will emulate a media eject event.</span></span> <span data-ttu-id="b4fe1-128">Il servizio può inoltre provare di nuovo a eseguire il comando o di ristabilire la connessione al dispositivo remoto.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-128">In addition, the service may re-try the command or try to re-establish the connection to the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-129">**CurrentAlternateSettings**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-129">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-130">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-132">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ usbdevice**.**CurrentConfigValue**")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-133">Matrice che contiene le impostazioni alternative per ogni interfaccia nella configurazione corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-133">An array that contains the alternate settings for each interface in the current configuration of the device.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-134">**CurrentConfigValue**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-134">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-135">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-137">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ usbdevice**.**CurrentAlternateSettings**")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-138">Configurazione attualmente selezionata per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-138">The configuration currently selected for the device.</span></span> <span data-ttu-id="b4fe1-139">Se questo valore è zero, il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-139">If this value is zero, the Device is not configured.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-140">**DeviceReleaseNumber**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-140">**DeviceReleaseNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-141">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-143">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bcdDevice")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdDevice")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-144">Numero di rilascio del dispositivo in formato BCD.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-144">The device release number in BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-145">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-145">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-148">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| iManufacturer")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iManufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-149">Stringa del produttore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-149">The manufacturer string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-150">**MaxPacketSize**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-150">**MaxPacketSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-151">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-151">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-153">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bMaxPacketSize")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bMaxPacketSize")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-154">Dimensioni massime del pacchetto per l'endpoint USB zero.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-154">The maximum packet size for the USB zero endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-155">**NumberOfConfigs**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-155">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-156">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-156">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-158">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bNumConfigurations")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bNumConfigurations")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-159">Il numero di configurazioni del dispositivo definite per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-159">The number of device configurations that are defined for the Device.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-160">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-160">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-163">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| IProduct")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iProduct")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-164">Stringa di prodotto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-164">The product string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-165">**ProductID**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-165">**ProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-166">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-168">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| idProduct")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idProduct")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-169">ID prodotto assegnato al dispositivo dal produttore.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-169">The product ID assigned to the device by manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-170">**ProtocolCode**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-170">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-171">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-173">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bDeviceProtocol")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-174">Codice del protocollo USB.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-174">The USB protocol code.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-175">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-175">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-178">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| iSerialNumber")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iSerialNumber")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-179">Numero di serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-179">The serial number of the device.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-180">**SubclassCode**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-180">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-181">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-181">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-183">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bDeviceSubClass")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceSubClass")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-184">Codice della sottoclasse USB.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-184">The USB subclass code.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-185">**USBVersion**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-185">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-186">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-188">Versione USB più recente supportata dal dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-188">The latest USB Version supported by the USB Device.</span></span> <span data-ttu-id="b4fe1-189">La proprietà è espressa come un valore decimale (BCD) con codifica binaria che contiene un separatore decimale compreso tra il secondo e il terzo.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-189">The property is expressed as a binary-coded decimal (BCD) that contains a decimal point between the 2nd and 3rd digits.</span></span> <span data-ttu-id="b4fe1-190">Ad esempio, il valore 0x201 indica che la versione 2,01 è supportata.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-190">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-191">**USBVersionInBCD**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-191">**USBVersionInBCD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-192">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-194">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| bcdUSB")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdUSB")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-195">Il numero di specifica USB a cui è conforme il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-195">The USB specification number that the device complies with.</span></span> <span data-ttu-id="b4fe1-196">Questa proprietà è formattata con il formato BCD.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-196">This property is formatted with BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="b4fe1-197">**VendorID**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-197">**VendorID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4fe1-198">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b4fe1-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4fe1-200">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification. USB-se il \| descrittore di dispositivo standard \| idVendor")</span><span class="sxs-lookup"><span data-stu-id="b4fe1-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idVendor")</span></span>
</dt> </dl>

<span data-ttu-id="b4fe1-201">ID del fornitore assegnato al dispositivo da USB.org.</span><span class="sxs-lookup"><span data-stu-id="b4fe1-201">The vendor ID assigned to the device by USB.org.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4fe1-202">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4fe1-202">Requirements</span></span>



| <span data-ttu-id="b4fe1-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4fe1-203">Requirement</span></span> | <span data-ttu-id="b4fe1-204">Valore</span><span class="sxs-lookup"><span data-stu-id="b4fe1-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fe1-205">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4fe1-205">Minimum supported client</span></span><br/> | <span data-ttu-id="b4fe1-206">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b4fe1-206">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b4fe1-207">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4fe1-207">Minimum supported server</span></span><br/> | <span data-ttu-id="b4fe1-208">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b4fe1-208">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b4fe1-209">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b4fe1-209">Namespace</span></span><br/>                | <span data-ttu-id="b4fe1-210">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b4fe1-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b4fe1-211">MOF</span><span class="sxs-lookup"><span data-stu-id="b4fe1-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4fe1-212"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4fe1-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4fe1-213">DLL</span><span class="sxs-lookup"><span data-stu-id="b4fe1-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4fe1-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b4fe1-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b4fe1-215">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4fe1-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4fe1-216">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b4fe1-216">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

