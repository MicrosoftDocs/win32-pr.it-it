---
title: Interfaccia INapSystemHealthValidator (NapSystemHealthValidator.h)
description: Deve essere implementato dagli sviluppatori SHV per consentire al sistema di Protezione accesso alla rete di comunicare con un'istanza shv.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- Interfaccia INapSystemHealthValidator NAP
- Interfaccia INapSystemHealthValidator nap , descritta
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7310afe1c61dd61344bd1ed355f78735dc7785f9016bbcbb702073b2a06feba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686061"
---
# <a name="inapsystemhealthvalidator-interface"></a>Interfaccia INapSystemHealthValidator

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapSystemHealthValidator** fornisce metodi che devono essere implementati dagli sviluppatori SHV per consentire al sistema di Protezione accesso alla rete di comunicare con un'istanza shv.

## <a name="members"></a>Membri

**L'interfaccia INapSystemHealthValidator** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthValidator** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **INapSystemHealthValidator.**



| Metodo                                                                                   | Descrizione                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidator::Validate**](inapsystemhealthvalidator-validate-method.md) | Il sistema di Protezione accesso alla rete chiama questo metodo definito dall'applicazione per convalidare [**l'oggetto SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ricevuto da un client. <br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

