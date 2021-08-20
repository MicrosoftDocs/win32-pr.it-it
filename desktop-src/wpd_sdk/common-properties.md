---
description: Windows Dispositivi portatili (WPD) supporta le proprietà seguenti dei parametri di comando.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Parametri del comando (PortableDevice.h)
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
ms.openlocfilehash: e5c58652c27d62e2954e86b9170e2f0a2d4ae4021743ced769adbf46a1f082b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431058"
---
# <a name="command-parameters"></a>Parametri dei comandi

Windows Dispositivi portatili (WPD) supporta le proprietà seguenti dei parametri di comando.




| **Proprietà**                                            | **VarType**     | **Descrizione**                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **INFORMAZIONI COMUNI SUL CLIENT DELLE PROPRIETÀ WPD \_ \_ \_ \_**          | **VT \_ UNKNOWN** | Interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) utilizzata dal driver per identificare il client.                                                             |
| **CONTESTO DELLE INFORMAZIONI CLIENT \_ COMUNI \_ DELLA \_ PROPRIETÀ \_ \_ WPD** | **VT \_ LPWSTR**  | Contesto specificato dal driver che identifica un client per tutte le operazioni successive.                                                                                          |
| **CATEGORIA DI COMANDI \_ COMUNI \_ DELLA PROPRIETÀ \_ \_ WPD**            | **VT \_ CLSID**   | Parte **GUID** del **valore PROPERTYKEY** del comando.                                                                                                            |
| **ID COMANDO COMUNE DELLA PROPRIETÀ WPD \_ \_ \_ \_**                  | **Interfaccia utente \_ VT4**     | Parte PID (Persistent Unique ID) del **valore PROPERTYKEY** del comando.                                                                                          |
| **DESTINAZIONE COMANDO COMUNE DELLA PROPRIETÀ WPD \_ \_ \_ \_**              | **VT \_ LPWSTR**  | Identificatore dell'oggetto di destinazione.                                                                                                                                                |
| **CODICE DI ERRORE COMUNE \_ \_ DEL DRIVER DELLA \_ \_ PROPRIETÀ \_ WPD**          | **Interfaccia utente \_ VT4**     | Codice di errore specifico del driver restituito da un driver WPD.                                                                                                                       |
| **HRESULT COMUNE \_ DELLA \_ PROPRIETÀ WPD \_**                      | **ERRORE \_ VT**   | Valore **HRESULT** restituito da un driver WPD per una determinata operazione.                                                                                                   |
| **ID OGGETTO \_ COMUNI DELLE PROPRIETÀ \_ WPD \_ \_**                  | **VT \_ UNKNOWN** | Interfaccia [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) di tipo **variant VT \_ LPWSTR** che contiene un elenco di identificatori di oggetto. |
| **ID UNIVOCI \_ \_ PERSISTENTI COMUNI DELLE PROPRIETÀ \_ \_ \_ WPD**      | **VT \_ UNKNOWN** | Interfaccia [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) di tipo **variant VT \_ LPWSTR** che contiene un elenco di PIN.               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi**](properties-and-attributes.md)
</dt> </dl>

 

 




