---
title: Interfaccia INapSystemHealthValidator (NapSystemHealthValidator. h)
description: Deve essere implementato dagli sviluppatori di servizio di convalida integrità per consentire al sistema NAP di comunicare con un servizio di convalida dell'integrità.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- NAP interfaccia INapSystemHealthValidator
- Interfaccia NAP di INapSystemHealthValidator, descrizione
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
ms.openlocfilehash: cce4d47555926c2a3ad5b06315521fea23503d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740903"
---
# <a name="inapsystemhealthvalidator-interface"></a>Interfaccia INapSystemHealthValidator

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapSystemHealthValidator** fornisce metodi che devono essere implementati dagli sviluppatori di servizio di convalida dell'integrità di sistema per consentire al sistema NAP di comunicare con un servizio di convalida dell'integrità

## <a name="members"></a>Membri

L'interfaccia **INapSystemHealthValidator** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthValidator** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapSystemHealthValidator** dispone di questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidator:: Validate**](inapsystemhealthvalidator-validate-method.md) | Il sistema NAP chiama il metodo definito dall'applicazione per convalidare il [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ricevuto da un client. <br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

