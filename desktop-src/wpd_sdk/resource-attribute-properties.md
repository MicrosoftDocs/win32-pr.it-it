---
description: Dispositivi portatili Windows supporta le seguenti proprietà dell'attributo di risorsa.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Proprietà degli attributi delle risorse (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 64f4f394fcd91d50f323a8e46a9556daa6a8dbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332107"
---
# <a name="resource-attribute-properties"></a>Proprietà degli attributi delle risorse

Dispositivi portatili Windows supporta le seguenti proprietà dell'attributo di risorsa.



| Proprietà                                    | VarType         | Descrizione                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_chiave di \_ risorsa dell'attributo della risorsa WPD \_ \_** | **VT \_ sconosciuto** | Si tratta di un [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) contenente un singolo valore, ovvero la chiave che identifica la risorsa.                     |
| **\_formato dell' \_ attributo della risorsa WPD \_**        | **\_CLSID VT**   | Valore GUID che specifica il formato della risorsa. Vedere [formati oggetto](object-format-guids.md) per un elenco di formati definiti da dispositivi portatili Windows. |
| **\_ \_ dimensioni totali dell'attributo della risorsa WPD \_ \_**   | **\_UI8 VT**     | Dimensioni totali, in byte, dei dati della risorsa.                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Questi attributi vengono restituiti dal metodo [**IPortableDeviceResources:: GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




