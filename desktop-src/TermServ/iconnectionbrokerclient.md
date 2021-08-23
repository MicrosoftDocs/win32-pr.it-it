---
title: Interfaccia IConnectionBrokerClient (Cbclient.h)
description: Fornisce i metodi necessari per usare il client Connessione Desktop remoto Broker.
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- Interfaccia IConnectionBrokerClient Servizi Desktop remoto
- Interfaccia IConnectionBrokerClient Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IConnectionBrokerClient
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87c30729a5ec78e5275a6c2a1c0d9d139b857c3c7ea10f666ba09b7fceed256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059159"
---
# <a name="iconnectionbrokerclient-interface"></a>Interfaccia IConnectionBrokerClient

Fornisce i metodi necessari per usare il client Connessione Desktop remoto Broker.

Questa interfaccia viene implementata dal sistema. Per ottenere un'istanza di questa interfaccia, usare la [**funzione CBCreateClientInstance.**](cbcreateclientinstance.md)

## <a name="members"></a>Membri

**L'interfaccia IConnectionBrokerClient** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IConnectionBrokerClient** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IConnectionBrokerClient** include questi metodi.



| Metodo                                                         | Descrizione                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) | Richiede informazioni sul computer di destinazione in cui deve essere reindirizzata la connessione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                       |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Cbclient.h</dt> </dl>      |
| Libreria<br/>                  | <dl> <dt>Cbclient.lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IConnectionBrokerClient è definito come D6818DF2-8338-4EB7-AD77-DE210817987C<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CBCreateClientInstance**](cbcreateclientinstance.md)
</dt> </dl>

 

