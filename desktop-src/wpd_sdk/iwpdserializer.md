---
description: "L'interfaccia IWpdSerializer viene utilizzata dal driver di dispositivo per serializzare le interfacce IPortableDeviceValues da e verso i buffer dei dati non elaborati utilizzati per comunicare con l'applicazione. Non è necessario che le applicazioni utilizzino questa interfaccia, perché i dati vengono serializzati e deserializzati automaticamente durante la chiamata a IPortableDevice:: SendCommand. per ottenere questa interfaccia, chiamare CoCreateInstance e passare IID \\_ IWpdSerializer."
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: Interfaccia IWpdSerializer (PortableDeviceTypes. h)
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
ms.openlocfilehash: dde4bfeea596ccc2691323d484f5583d55ade621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330431"
---
# <a name="iwpdserializer-interface"></a>Interfaccia IWpdSerializer

L'interfaccia **IWpdSerializer** viene utilizzata dal driver di dispositivo per serializzare le interfacce [**IPortableDeviceValues**](iportabledevicevalues.md) da e verso i buffer dei dati non elaborati utilizzati per comunicare con l'applicazione.

Non è necessario che le applicazioni utilizzino questa interfaccia, perché i dati vengono serializzati e deserializzati automaticamente quando si chiama [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

Per ottenere questa interfaccia, chiamare **CoCreateInstance** e passare l' **IID \_ IWpdSerializer**.

## <a name="members"></a>Membri

L'interfaccia **IWpdSerializer** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWpdSerializer** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWpdSerializer** dispone di questi metodi.



| Metodo                                                                                          | Descrizione                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md) | Serializza un'interfaccia **IPortableDeviceValues** inviata in una matrice di byte allocata.<br/>                |
| [**GetIPortableDeviceValuesFromBuffer**](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | Deserializza una matrice di byte in un'interfaccia **IPortableDeviceValues** .<br/>                                  |
| [**GetSerializedSize**](iwpdserializer-getserializedsize.md)                                   | Calcola la dimensione del buffer necessaria per mantenere un'interfaccia **IPortableDeviceValues** serializzata.<br/> |
| [**WriteIPortableDeviceValuesToBuffer**](iwpdserializer-writeiportabledevicevaluestobuffer.md) | Serializza un'interfaccia **IPortableDeviceValues** in una matrice di byte allocata dal chiamante.<br/>                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce driver**](driver-interfaces.md)
</dt> </dl>

 

