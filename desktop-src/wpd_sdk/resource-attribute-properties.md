---
description: Windows Dispositivi portabili supporta le proprietà degli attributi delle risorse seguenti.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Proprietà degli attributi delle risorse (PortableDevice.h)
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
ms.openlocfilehash: 956cd349089afb00a1350bf32e8f06acd5747599f6d5a731e4bf5d8dd1c96295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928071"
---
# <a name="resource-attribute-properties"></a>Proprietà degli attributi delle risorse

Windows Dispositivi portabili supporta le proprietà degli attributi delle risorse seguenti.



| Proprietà                                    | VarType         | Descrizione                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CHIAVE DI RISORSA \_ \_ DELL'ATTRIBUTO \_ DELLA RISORSA \_ WPD** | **VT \_ UNKNOWN** | Si tratta di [**un oggetto IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) contenente un singolo valore, ovvero la chiave che identifica la risorsa.                     |
| **FORMATO DELL'ATTRIBUTO DELLA RISORSA WPD \_ \_ \_**        | **VT \_ CLSID**   | Valore GUID che specifica il formato della risorsa. Vedere [Formati di oggetto](object-format-guids.md) per un elenco di formati definiti da Windows dispositivi portatili. |
| **DIMENSIONI TOTALI \_ DELL'ATTRIBUTO DELLA RISORSA \_ \_ \_ WPD**   | **Interfaccia utente \_ VT8**     | Dimensioni totali dei dati delle risorse, in byte.                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Questi attributi vengono restituiti dal [**metodo IPortableDeviceResources::GetResourceAttributes.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




