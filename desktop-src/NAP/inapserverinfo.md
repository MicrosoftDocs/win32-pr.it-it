---
title: Interfaccia INapServerInfo (NapServerManagement. h)
description: I client di gestione (ad esempio, i provider WMI o gli strumenti da riga di comando) utilizzano per eseguire una query sullo stato del sistema server protezione accesso alla rete.
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- NAP interfaccia INapServerInfo
- Interfaccia NAP di INapServerInfo, descrizione
topic_type:
- apiref
api_name:
- INapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec17e3303fe4af4d359279de6c5fa7aa5f34d409
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301813"
---
# <a name="inapserverinfo-interface"></a>Interfaccia INapServerInfo

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapServerInfo** fornisce i metodi che i client di gestione (ad esempio, i provider WMI o gli strumenti da riga di comando) utilizzano per eseguire una query sullo stato del sistema server protezione accesso alla rete.

## <a name="members"></a>Membri

L'interfaccia **INapServerInfo** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapServerInfo** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapServerInfo** dispone di questi metodi.



| Metodo                                                                                                                   | Descrizione                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**INapServerInfo::GetFailureCategoryMappings**](inapserverinfo-getfailurecategorymappings-method.md)                   | Recupera i mapping delle categorie di errore per un oggetto di convalida integrità specificato.<br/> |
| [**INapServerInfo::GetNapServerInfo**](inapserverinfo-getnapserverinfo-method.md)                                       | Recupera le informazioni sul server NAP.<br/>                  |
| [**INapServerInfo::GetRegisteredSystemHealthValidators**](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | Recupera un elenco di SHV registrati.<br/>                         |



 

## <a name="remarks"></a>Commenti

Questi metodi forniscono solo informazioni statiche sul server NAP e sui relativi componenti nel sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>NapServerManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapServerManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

