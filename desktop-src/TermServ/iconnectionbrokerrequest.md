---
title: Interfaccia IConnectionBrokerRequest (Cbclient. h)
description: Fornisce i metodi necessari per ottenere i risultati del metodo asincrono IConnectionBrokerClient GetTargetInfo.
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- Interfaccia IConnectionBrokerRequest Servizi Desktop remoto
- Interfaccia IConnectionBrokerRequest Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb95427aee37053b6979cb1a12ce7b5d1942c2fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743663"
---
# <a name="iconnectionbrokerrequest-interface"></a>Interfaccia IConnectionBrokerRequest

Fornisce i metodi necessari per ottenere i risultati del metodo asincrono [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

Questa interfaccia viene implementata dal sistema. Un'istanza di questa interfaccia viene fornita al chiamante con il metodo [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

## <a name="members"></a>Membri

L'interfaccia **IConnectionBrokerRequest** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IConnectionBrokerRequest** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IConnectionBrokerRequest** dispone di questi metodi.



| Metodo                                                      | Descrizione                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) | Chiamato per determinare lo stato di una richiesta asincrona.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                        |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>     |
| IID<br/>                      | IID \_ IConnectionBrokerRequest è definito come 25114427-ED5D-46a6-AF53-C62D33A4108E<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

