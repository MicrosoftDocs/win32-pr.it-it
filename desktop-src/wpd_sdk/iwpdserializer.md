---
description: L'interfaccia IWpdSerializer viene usata dal driver di dispositivo per serializzare le interfacce IPortableDeviceValues da e verso i buffer di dati non elaborati usati per comunicare con l'applicazione. Le applicazioni non devono usare questa interfaccia, perché i dati vengono serializzati e deserializzati automaticamente quando si chiama IPortableDevice::SendCommand.Per ottenere questa interfaccia, chiamare CoCreateInstance e passare IID \_ IWpdSerializer.
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: Interfaccia IWpdSerializer (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 51bb44a7ffec600ff6a059815f096b6920095ece1abd6606e9449045137dbc61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704461"
---
# <a name="iwpdserializer-interface"></a>Interfaccia IWpdSerializer

**L'interfaccia IWpdSerializer** viene usata dal driver di dispositivo per serializzare le interfacce [**IPortableDeviceValues**](iportabledevicevalues.md) da e verso i buffer di dati non elaborati usati per comunicare con l'applicazione.

Le applicazioni non devono usare questa interfaccia, perché i dati vengono serializzati e deserializzati automaticamente quando si chiama [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

Per ottenere questa interfaccia, chiamare **CoCreateInstance** e passare **IID \_ IWpdSerializer**.

## <a name="members"></a>Membri

**L'interfaccia IWpdSerializer** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWpdSerializer** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IWpdSerializer.**



| Metodo                                                                                          | Descrizione                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md) | Serializza **un'interfaccia IPortableDeviceValues inviata** in una matrice di byte allocata.<br/>                |
| [**GetIPortableDeviceValuesFromBuffer**](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | Deserializza una matrice di byte in **un'interfaccia IPortableDeviceValues.**<br/>                                  |
| [**GetSerializedSize**](iwpdserializer-getserializedsize.md)                                   | Calcola le dimensioni del buffer necessarie per contenere **un'interfaccia IPortableDeviceValues serializzata.**<br/> |
| [**WriteIPortableDeviceValuesToBuffer**](iwpdserializer-writeiportabledevicevaluestobuffer.md) | Serializza **un'interfaccia IPortableDeviceValues** in una matrice di byte allocata dal chiamante.<br/>                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce del driver**](driver-interfaces.md)
</dt> </dl>

 

