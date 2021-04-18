---
description: I dispositivi portatili Windows supportano le seguenti proprietà di associazione di rete.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Proprietà associazione di rete (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41e40e456d4671d1aa8fb190274afd2f5ace98b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328569"
---
# <a name="network-association-properties"></a>Proprietà dell'associazione di rete

I dispositivi portatili Windows supportano le seguenti proprietà di associazione di rete.



| Proprietà                                                  | VarType                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ \_ identificatori di rete dell'host di associazione di rete WPD \_** | **VT \_ vettore \| VT \_ UI1** | Elenco di identificatori host EUI-64 validi per questa associazione. Si tratta di una matrice di byte che contiene un numero integrale di indirizzi di rete fisica EUI-64. Questi valori EUI-64 sono gli indirizzi di rete fisici disponibili nell'host al momento dell'associazione di rete. Se l'host dispone di indirizzi di rete fisica MAC-48 (tipici di reti IPv4), ogni indirizzo MAC-48 verrà codificato nell'indirizzo EUI-64 come due metà dell'indirizzo MAC-48 separato da FF-FF.<br/> |
| **\_ \_ X509V3SEQUENCE associazione di rete WPD \_**             | **VT \_ vettore \| VT \_ UI1** | Sequenza di certificati X. 509 v3 da fornire per l'autenticazione del server TLS.                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




