---
description: Fornisce i metodi che WUA può usare per raccogliere informazioni sul token dell'endpoint.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Interfaccia IUpdateEndpointAuthToken (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7b5afa1e9039b7f210dfbf71c8bceff4a7b438b413844a7a7e55dec0fd9fea8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855761"
---
# <a name="iupdateendpointauthtoken-interface"></a>Interfaccia IUpdateEndpointAuthToken

Fornisce i metodi che WUA può usare per raccogliere informazioni sul token dell'endpoint.

## <a name="members"></a>Membri

**L'interfaccia IUpdateEndpointAuthToken** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUpdateEndpointAuthToken** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IUpdateEndpointAuthToken.**



| Metodo                                                                                | Descrizione                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**ServiceID**](iupdateendpointauthtoken-serviceid.md)                               | Ottiene l'identificatore del servizio da autenticare.<br/>                                                          |
| [**SigningKey**](iupdateendpointauthtoken-signingkey.md)                             | Ottiene la chiave utilizzata per firmare i messaggi in uscita tra il computer client e il sercvice.<br/>                        |
| [**TokenData**](iupdateendpointauthtoken-tokendata.md)                               | Ottiene i dati XML (inviati in transito) che rappresentano il token. <br/>                                               |
| [**TokenReferenceAttached**](iupdateendpointauthtoken-tokenreferenceattached.md)     | Ottiene il formato XML di un riferimento associato al token.<br/>                                                       |
| [**TokenReferenceUnattached**](iupdateendpointauthtoken-tokenreferenceunattached.md) | Ottiene il formato XML di un riferimento non associato al token.<br/>                                                     |
| [**TokenType**](iupdateendpointauthtoken-tokentype.md)                               | Ottiene il tipo di token dell'endpoint WS-Security, ad esempio un token SAML (Security Assertion Markup Language) 1.1. <br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional solo con app desktop SP3 \[\]<br/>                   |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con solo app desktop SP3 \[\]<br/>                |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>UpdateEndpointAuth.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
