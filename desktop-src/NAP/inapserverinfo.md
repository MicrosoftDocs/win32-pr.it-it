---
title: Interfaccia INapServerInfo (NapServerManagement.h)
description: I client di gestione ,ad esempio i provider WMI o gli strumenti da riga di comando, usano per eseguire query sullo stato del sistema server di Protezione accesso alla rete.
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- Interfaccia INapServerInfo nap
- Interfaccia INapServerInfo nap , descritta
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
ms.openlocfilehash: 556c2a5b7e7545038995d5091d46931352f9ee32bddfa31b91237dfa54d69620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626101"
---
# <a name="inapserverinfo-interface"></a>Interfaccia INapServerInfo

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapServerInfo** fornisce metodi che i client di gestione ,ad esempio i provider WMI o gli strumenti da riga di comando, usano per eseguire query sullo stato del sistema server di Protezione accesso alla rete.

## <a name="members"></a>Membri

**L'interfaccia INapServerInfo** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapServerInfo** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **INapServerInfo.**



| Metodo                                                                                                                   | Descrizione                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**INapServerInfo::GetFailureCategoryMappings**](inapserverinfo-getfailurecategorymappings-method.md)                   | Recupera i mapping della categoria di errore per un'istanza shv specificata.<br/> |
| [**INapServerInfo::GetNapServerInfo**](inapserverinfo-getnapserverinfo-method.md)                                       | Recupera informazioni sul server di Protezione accesso alla rete.<br/>                  |
| [**INapServerInfo::GetRegisteredSystemHealthValidators**](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | Recupera un elenco di shv registrati.<br/>                         |



 

## <a name="remarks"></a>Commenti

Questi metodi forniscono solo informazioni statiche sul server di Protezione accesso alla rete e sui relativi componenti nel sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

