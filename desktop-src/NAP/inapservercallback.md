---
title: Interfaccia INapServerCallback (NapSystemHealthValidator. h)
description: SHV utilizzare per segnalare il completamento asincrono della richiesta.
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- NAP interfaccia INapServerCallback
- Interfaccia NAP di INapServerCallback, descrizione
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18aaf900a603a577ec12835441c67c20453a5dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475268"
---
# <a name="inapservercallback-interface"></a>Interfaccia INapServerCallback

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapServerCallback** fornisce un metodo che SHV USA per segnalare il completamento della richiesta asincrona.

## <a name="members"></a>Membri

L'interfaccia **INapServerCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapServerCallback** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapServerCallback** dispone di questi metodi.



| Metodo                                                                         | Descrizione                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapServerCallback:: OnComplete**](inapservercallback-oncomplete-method.md) | Usato da SHV per segnalare il completamento della richiesta asincrona.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

