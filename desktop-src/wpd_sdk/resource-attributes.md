---
description: Windows Dispositivi portabili supporta gli attributi di risorsa seguenti.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Attributi delle risorse (PortableDevice.h)
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
ms.openlocfilehash: 303f43f1061dd9d8b05855b3c2af94a1ace3c071c12b308303b1524b255a6133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963515"
---
# <a name="resource-attributes"></a>Attributi delle risorse

Windows Dispositivi portabili supporta gli attributi di risorsa seguenti. Questi attributi vengono restituiti dai metodi seguenti:

-   [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| Attributo                                                  | VarType      | Descrizione                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **L'ATTRIBUTO \_ DELLA RISORSA WPD PUÒ ESSERE \_ \_ \_ ELIMINATO**                  | **VT \_ BOOL** | Valore booleano che specifica se un client dispone dell'autorizzazione per eliminare la risorsa. Se assente, si presuppone che sia false.                |
| **ATTRIBUTO RISORSA WPD \_ \_ \_ \_ LEGGIBILE**                    | **VT \_ BOOL** | Valore booleano che specifica se un client dispone dell'autorizzazione per aprire la risorsa per l'accesso in lettura. Se assente, si presuppone che sia False.  |
| **L'ATTRIBUTO \_ DELLA RISORSA WPD PUÒ \_ \_ \_ SCRIVERE**                   | **VT \_ BOOL** | Valore booleano che specifica se un client dispone dell'autorizzazione per aprire la risorsa per l'accesso in scrittura. Se assente, si presuppone che sia false. |
| **DIMENSIONI OTTIMALI DEL \_ BUFFER DI \_ LETTURA \_ DELL'ATTRIBUTO DELLA \_ \_ RISORSA \_ WPD**  | **VT \_ UI4**  | Dimensioni consigliate del buffer che un chiamante deve usare per le operazioni di lettura memorizzate nel buffer dalla risorsa.                                                  |
| **DIMENSIONI OTTIMALI DEL \_ BUFFER DI \_ SCRITTURA \_ DELL'ATTRIBUTO \_ \_ RISORSA \_ WPD** | **VT \_ UI4**  | Dimensioni del buffer consigliate che un chiamante deve usare per le scritture memorizzate nel buffer nella risorsa.                                                   |
| **DIMENSIONI TOTALI \_ DELL'ATTRIBUTO DELLA RISORSA \_ \_ \_ WPD**                  | **Interfaccia utente \_ VT8**  | Dimensioni totali dei dati delle risorse, in byte.                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà**](properties-and-attributes.md)
</dt> </dl>

 

 




