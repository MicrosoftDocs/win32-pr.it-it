---
description: Dispositivi portatili Windows (WPD) supporta le seguenti proprietà dei parametri del comando.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Parametri del comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7687488c38f95fd6d7e7b69d64ad6ae32631700d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330248"
---
# <a name="command-parameters"></a>Parametri dei comandi

Dispositivi portatili Windows (WPD) supporta le seguenti proprietà dei parametri del comando.




| **Proprietà**                                            | **VarType**     | **Descrizione**                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_Proprietà WPD \_ \_ informazioni client \_ comuni**          | **VT \_ sconosciuto** | Interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) utilizzata dal driver per identificare il client.                                                             |
| **\_Proprietà WPD \_ \_ \_ contesto delle informazioni client comuni \_** | **\_LPWSTR VT**  | Contesto specificato dal driver che identifica un client per tutte le operazioni successive.                                                                                          |
| **\_categoria di \_ \_ comandi comune della proprietà \_ WPD**            | **\_CLSID VT**   | Parte del **GUID** del valore **PropertyKey** del comando.                                                                                                            |
| **\_ \_ \_ ID comando comune della proprietà WPD \_**                  | **\_UI4 VT**     | Porzione di ID univoco permanente (PID) del valore **PropertyKey** del comando.                                                                                          |
| **\_ \_ \_ destinazione comando comune della proprietà WPD \_**              | **\_LPWSTR VT**  | Identificatore dell'oggetto di destinazione.                                                                                                                                                |
| **\_codice di \_ \_ errore del driver comune della proprietà \_ WPD \_**          | **\_UI4 VT**     | Codice di errore specifico del driver restituito da un driver WPD.                                                                                                                       |
| **\_ \_ HRESULT comune della proprietà WPD \_**                      | **\_errore VT**   | Valore **HRESULT** restituito da un driver WPD per un'operazione specifica.                                                                                                   |
| **\_ \_ \_ ID oggetto comuni della proprietà WPD \_**                  | **VT \_ sconosciuto** | Interfaccia [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) di tipo Variant **VT \_ LPWSTR** che contiene un elenco di identificatori di oggetto. |
| **\_Proprietà WPD \_ gli \_ \_ ID univoci permanenti comuni \_**      | **VT \_ sconosciuto** | Interfaccia [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) di tipo Variant **VT \_ LPWSTR** che contiene un elenco di PID.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi**](properties-and-attributes.md)
</dt> </dl>

 

 




