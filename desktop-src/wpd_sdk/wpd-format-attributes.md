---
description: 'Per Windows 7, i dispositivi portatili Windows supportano i seguenti attributi per i formati in un servizio del dispositivo. Questi attributi vengono restituiti dal metodo IPortableDeviceServiceCapabilities:: GetFormatAttributes.'
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: Attributi di formato (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 559f731ec7d61007b05e4625ff67488b5ef482fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328963"
---
# <a name="format-attributes"></a>Attributi di formato

Per Windows 7, i dispositivi portatili Windows supportano i seguenti attributi per i formati in un servizio del dispositivo. Questi attributi vengono restituiti dal metodo [**IPortableDeviceServiceCapabilities:: GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) .




| **Attributo**                        | **VarType**    | **Descrizione**                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ MIMETYPE attributo formato \_ WPD** | **\_LPWSTR VT** | Tipo MIME del formato.                                                                                                     |
| **\_ \_ nome attributo formato \_ WPD**     | **\_LPWSTR VT** | Stringa che specifica il nome descrittivo per lo script del formato. I caratteri validi sono alfanumerici \[ a-Za-z0-9 \] è \_ '. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi**](properties-and-attributes.md)
</dt> </dl>

 

 




