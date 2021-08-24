---
title: Interfaccia INapSoHConstructor (NapProtocol.h)
description: Vengono usati da SHAs per costruire SoHRequests e da SHV per costruire SoHResponses.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- Interfaccia INapSoHConstructor NAP
- Interfaccia INapSoHConstructor NAP , descritta
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ceb9e927e1ac65f21a3ff457922e1bd475b8327ac2525b2af7afefa6cb173f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037851"
---
# <a name="inapsohconstructor-interface"></a>Interfaccia INapSoHConstructor

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapSoHConstructor** fornisce metodi usati dagli SHA per costruire [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) e da SHV per costruire **SoHResponses**.

## <a name="members"></a>Membri

**L'interfaccia INapSoHConstructor** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSoHConstructor** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia INapSoHConstructor** include questi metodi.



| Metodo                                                                                   | Descrizione                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [**INapSoHConstructor::AppendAttribute**](inapsohconstructor-appendattribute-method.md) | Aggiunge un TLV alla fine del buffer SoH.<br/> |
| [**INapSoHConstructor::GetSoH**](inapsohconstructor-getsoh-method.md)                   | Recupera il pacchetto SoH costruito.<br/>    |
| [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md)           | Inizializza il pacchetto SoH.<br/>              |
| [**INapSoHConstructor::Validate**](inapsohconstructor-validate-method.md)               | Verifica la validità del pacchetto SoH.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

