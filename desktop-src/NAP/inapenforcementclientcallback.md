---
title: Interfaccia INapEnforcementClientCallback (NapEnforcementClient. h)
description: I client di imposizione devono implementare per consentire a NapAgent di comunicare con loro.
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- NAP interfaccia INapEnforcementClientCallback
- Interfaccia NAP di INapEnforcementClientCallback, descrizione
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d5c7e066115a6d51879775d9b8cfab3cbe4888
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302716"
---
# <a name="inapenforcementclientcallback-interface"></a>Interfaccia INapEnforcementClientCallback

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'interfaccia **INapEnforcementClientCallback** fornisce metodi di callback che i client di imposizione devono implementare per consentire a napagent di comunicare con essi.

## <a name="members"></a>Membri

L'interfaccia **INapEnforcementClientCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapEnforcementClientCallback** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapEnforcementClientCallback** dispone di questi metodi.



| Metodo                                                                                                         | Descrizione                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientCallback:: getconnects**](inapenforcementclientcallback-getconnections-method.md)   | Usato da NapAgent per recuperare le connessioni.<br/>                         |
| [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) | Usato da NapAgent per informare il client di imposizione delle modifiche del rapporto di integrità.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



 

