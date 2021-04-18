---
description: Definisce il tipo di token che è possibile utilizzare per l'autenticazione con un endpoint.
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: Enumerazione UpdateEndpointAuthTokenType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointAuthTokenType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: c978841511b7cfff895a15936a41d169a8500927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305831"
---
# <a name="updateendpointauthtokentype-enumeration"></a>Enumerazione UpdateEndpointAuthTokenType

Definisce il tipo di token che è possibile utilizzare per l'autenticazione con un endpoint.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagUpdateEndpointAuthTokenType { 
  ueattInvalidTokenType  = 0x0,
  ueattSAML11Token       = 0X1
} UpdateEndpointAuthTokenType;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**ueattInvalidTokenType**
</dt> <dd>

Non è necessario alcun token di autenticazione.

</dd> <dt>

<span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**
</dt> <dd>

Il token di autenticazione per l'endpoint è un token WS-Security SAML (Security Assertion Markup Language) 1,1.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |



 

 




