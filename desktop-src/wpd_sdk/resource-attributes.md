---
description: I dispositivi portatili Windows supportano i seguenti attributi di risorse.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Attributi della risorsa (PortableDevice. h)
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
ms.openlocfilehash: 300add64d332dbc509bef6ec5bb2ad124f7a6b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332106"
---
# <a name="resource-attributes"></a>Attributi delle risorse

I dispositivi portatili Windows supportano i seguenti attributi di risorse. Questi attributi vengono restituiti dai metodi seguenti:

-   [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| Attributo                                                  | VarType      | Descrizione                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **l' \_ attributo della risorsa WPD \_ può essere \_ \_ eliminato**                  | **\_bool VT** | Valore booleano che specifica se un client dispone dell'autorizzazione per eliminare la risorsa. Se assente, si presuppone che sia false.                |
| **l'attributo della risorsa WPD è in \_ \_ grado di \_ \_ leggere**                    | **\_bool VT** | Valore booleano che specifica se un client dispone dell'autorizzazione per aprire la risorsa per l'accesso in lettura. Se assente, si presuppone che sia false.  |
| **l' \_ attributo della risorsa WPD \_ \_ può \_ scrivere**                   | **\_bool VT** | Valore booleano che specifica se un client dispone dell'autorizzazione per aprire la risorsa per l'accesso in scrittura. Se assente, si presuppone che sia false. |
| **\_dimensione del \_ \_ buffer di \_ lettura ottimale dell' \_ attributo \_ della risorsa WPD**  | **\_UI4 VT**  | Dimensione del buffer consigliata che un chiamante deve usare per le letture memorizzate nel buffer dalla risorsa.                                                  |
| **\_dimensioni del \_ \_ buffer di scrittura ottimali dell'attributo \_ della \_ risorsa WPD \_** | **\_UI4 VT**  | Dimensione del buffer consigliata che un chiamante deve usare per le scritture memorizzate nel buffer sulla risorsa.                                                   |
| **\_ \_ dimensioni totali dell'attributo della risorsa WPD \_ \_**                  | **\_UI8 VT**  | Dimensioni totali, in byte, dei dati della risorsa.                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà**](properties-and-attributes.md)
</dt> </dl>

 

 




