---
title: Interfaccia INapSystemHealthValidationRequest2 (NapSystemHealthValidator.h)
description: Fornisce i metodi utilizzati per supportare i validator dell'integrità del sistema definiti dallo sviluppatore dell'applicazione.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- Interfaccia INapSystemHealthValidationRequest2 nap
- Interfaccia INapSystemHealthValidationRequest2 nap , descritta
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6438394120ecd901c6de6d7a8ccac40f742d9f73d27a36682de894d9c5a7ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620850"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a>Interfaccia INapSystemHealthValidationRequest2

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**L'interfaccia INapSystemHealthValidationRequest2** fornisce metodi usati per supportare i validator dell'integrità del sistema definiti dallo sviluppatore dell'applicazione.

> [!Note]  
> Questa interfaccia eredita tutti i metodi di [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) e deve essere usata.

 

## <a name="members"></a>Membri

**L'interfaccia INapSystemHealthValidationRequest2** eredita da [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md). **INapSystemHealthValidationRequest2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **INapSystemHealthValidationRequest2.**



| Metodo                                                                                                    | Descrizione                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest2::GetConfigId**](inapsystemhealthvalidationrequest2-getconfigid.md) | Recupera l'ID di configurazione in una richiesta di convalida.<br/> |



 

## <a name="remarks"></a>Commenti

Se shv non supporta [**INapComponentConfig3,**](inapcomponentconfig3.md)questa interfaccia non è applicabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

 





