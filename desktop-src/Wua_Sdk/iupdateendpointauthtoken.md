---
description: Fornisce i metodi che WUA può utilizzare per raccogliere informazioni sul token dell'endpoint.
ms.assetid: 52D22909-B926-426F-98C7-643C4469D021
title: Interfaccia IUpdateEndpointAuthToken (UpdateEndpointAuth. h)
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
ms.openlocfilehash: a5902b3c91b3ab12b311121bd7dcd8c415a68d6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485140"
---
# <a name="iupdateendpointauthtoken-interface"></a>Interfaccia IUpdateEndpointAuthToken

Fornisce i metodi che WUA può utilizzare per raccogliere informazioni sul token dell'endpoint.

## <a name="members"></a>Membri

L'interfaccia **IUpdateEndpointAuthToken** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUpdateEndpointAuthToken** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IUpdateEndpointAuthToken** dispone di questi metodi.



| Metodo                                                                                | Descrizione                                                                                                                 |
|:--------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**ServiceID**](iupdateendpointauthtoken-serviceid.md)                               | Ottiene l'identificatore del servizio da autenticare.<br/>                                                          |
| [**SigningKey**](iupdateendpointauthtoken-signingkey.md)                             | Ottiene la chiave utilizzata per firmare i messaggi in uscita tra il computer client e sercvice.<br/>                        |
| [**TokenData**](iupdateendpointauthtoken-tokendata.md)                               | Ottiene i dati XML (inviati in rete) che rappresenta il token. <br/>                                               |
| [**TokenReferenceAttached**](iupdateendpointauthtoken-tokenreferenceattached.md)     | Ottiene il formato XML di un riferimento associato al token.<br/>                                                       |
| [**TokenReferenceUnattached**](iupdateendpointauthtoken-tokenreferenceunattached.md) | Ottiene il formato XML di un riferimento non associato al token.<br/>                                                     |
| [**TokenType**](iupdateendpointauthtoken-tokentype.md)                               | Ottiene il tipo del token dell'endpoint, ad esempio un token WS-Security SAML (Security Assertion Markup Language) 1,1. <br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]<br/>                   |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]<br/>                |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
