---
description: Contiene i metodi utilizzati per negoziare il tipo di token utilizzato per l'autenticazione dell'endpoint di un servizio.
ms.assetid: F6177B24-C166-4BEC-83D6-3AD5B5B3CF08
title: Interfaccia IUpdateEndpointAuthProvider (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 071bc23bdf9d67412fef561c71e17fe81485984f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526683"
---
# <a name="iupdateendpointauthprovider-interface"></a>Interfaccia IUpdateEndpointAuthProvider

L'interfaccia **IUpdateEndpointAuthProvider** contiene i metodi usati per negoziare il tipo di token usato per autenticare l'endpoint di un servizio.

## <a name="members"></a>Membri

L'interfaccia **IUpdateEndpointAuthProvider** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUpdateEndpointAuthProvider** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IUpdateEndpointAuthProvider** dispone di questi metodi.



| Metodo                                                                                             | Descrizione                                                                                    |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)                           | Richiedere un token per l'endpoint del servizio usando le credenziali specificate.<br/>    |
| [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) | Restituisce il tipo preferito di token di autenticazione per l'endpoint del servizio.<br/> |



 

## <a name="remarks"></a>Commenti

WUA chiama il metodo [**GetPreferredEndpointTokenType**](iupdateendpointauthprovider-getpreferredendpointtokentype.md) di questa interfaccia per avviare il processo di negoziazione. Quando viene effettuata la chiamata, WUA passa l'identificatore del servizio, il tipo di endpoint implementato dal servizio e i tipi di token disponibili. L'implementazione di questa interfaccia restituisce quindi i tipi di token che preferisce usare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]<br/>                   |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]<br/>                |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



 

 
