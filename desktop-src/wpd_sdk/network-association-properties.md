---
description: Windows Dispositivi portatili supporta le proprietà di associazione di rete seguenti.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Proprietà associazione di rete (PortableDevice.h)
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
ms.openlocfilehash: ebad4534976d14e6b620a8e42b70e8ece68022201cec5235295d199e453ef818
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963530"
---
# <a name="network-association-properties"></a>Proprietà associazione di rete

Windows Dispositivi portatili supporta le proprietà di associazione di rete seguenti.



| Proprietà                                                  | VarType                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IDENTIFICATORI DI RETE HOST ASSOCIAZIONE DI RETE \_ \_ \_ \_ \_ WPD** | **VT \_ VECTOR \| VT \_ UI1** | Elenco di identificatori host EUI-64 validi per questa associazione. Matrice di byte che contiene un numero integrale di indirizzi di rete fisica EUI-64. Questi valori EUI-64 sono gli indirizzi di rete fisici disponibili nell'host in fase di associazione di rete. Se l'host ha indirizzi di rete fisica MAC-48 (tipici delle reti IPv4), ogni indirizzo MAC-48 verrà codificato nell'indirizzo EUI-64 come le due metà dell'indirizzo MAC-48 separato da FF-FF.<br/> |
| **ASSOCIAZIONE DI RETE WPD \_ \_ \_ X509V3SEQUENCE**             | **VT \_ VECTOR \| VT \_ UI1** | Sequenza di certificati X.509 v3 da ottenere per l'autenticazione del server TLS.                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




