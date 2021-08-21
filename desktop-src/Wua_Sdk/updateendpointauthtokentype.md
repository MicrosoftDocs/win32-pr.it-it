---
description: Definisce il tipo di token che possono essere usati per l'autenticazione con un endpoint.
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: Enumerazione UpdateEndpointAuthTokenType (UpdateEndpointAuth.h)
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
ms.openlocfilehash: b9e3efbff48097dcede12d5c8d3117171ef622f20a3bf017b12c6d3ce13a1c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814713"
---
# <a name="updateendpointauthtokentype-enumeration"></a>Enumerazione UpdateEndpointAuthTokenType

Definisce il tipo di token che possono essere usati per l'autenticazione con un endpoint.

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

Il token di autenticazione per l'endpoint è WS-Security token SAML (Security Assertion Markup Language) 1.1.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |



 

 




