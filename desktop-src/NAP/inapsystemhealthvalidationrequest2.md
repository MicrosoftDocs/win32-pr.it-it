---
title: Interfaccia INapSystemHealthValidationRequest2 (NapSystemHealthValidator. h)
description: Fornisce metodi utilizzati per supportare i validator di integrità del sistema definiti dallo sviluppatore di applicazioni.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- NAP interfaccia INapSystemHealthValidationRequest2
- Interfaccia NAP di INapSystemHealthValidationRequest2, descrizione
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
ms.openlocfilehash: 12fdbfc46578a4e64a92accc46f6b910a44dd946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302714"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a>Interfaccia INapSystemHealthValidationRequest2

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'interfaccia **INapSystemHealthValidationRequest2** fornisce i metodi utilizzati per supportare i validator dell'integrità di sistema definiti dallo sviluppatore di applicazioni.

> [!Note]  
> Questa interfaccia eredita tutti i metodi di [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) e deve essere usata in alternativa.

 

## <a name="members"></a>Membri

L'interfaccia **INapSystemHealthValidationRequest2** eredita da [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md). **INapSystemHealthValidationRequest2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapSystemHealthValidationRequest2** dispone di questi metodi.



| Metodo                                                                                                    | Descrizione                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest2::GetConfigId**](inapsystemhealthvalidationrequest2-getconfigid.md) | Recupera l'ID configurazione in una richiesta di convalida.<br/> |



 

## <a name="remarks"></a>Commenti

Se un servizio di convalida dell'integrità di sistema non supporta [**INapComponentConfig3**](inapcomponentconfig3.md), questa interfaccia non è applicabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

 





