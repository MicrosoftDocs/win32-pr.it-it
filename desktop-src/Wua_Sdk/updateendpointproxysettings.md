---
description: La struttura UpdateEndpointProxySettings definisce le impostazioni proxy usate per la richiesta di un token.
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: Struttura UpdateEndpointProxySettings (UpdateEndpointAuth.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointProxySettings
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: ed40016e930121ec12cf6ff21eb72da71e9e1f12ecb9b7ac9234b4d923c369df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106077"
---
# <a name="updateendpointproxysettings-structure"></a>Struttura UpdateEndpointProxySettings

La **struttura UpdateEndpointProxySettings** definisce le impostazioni proxy usate per la richiesta di un token.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagUpdateEndpointProxySettings {
  BSTR szProxyAddr;
  BSTR szBypassList;
  BSTR szUserName;
  BSTR szPassword;
} UpdateEndpointProxySettings;
```



## <a name="members"></a>Members

<dl> <dt>

**szProxyAddr**
</dt> <dd>

Nome DNS o indirizzo IP del server proxy da usare ,ad esempio "proxy.somecorp.com" o "192.168.0.4", oppure una stringa vuota se non deve essere usato alcun proxy.

</dd> <dt>

**szBypassList**
</dt> <dd>

Elenco di indirizzi host che devono ignorare il server proxy o una stringa vuota se tutti gli indirizzi host devono usare il server proxy

WUA non usa questi dati se **szProxyAddr** è vuoto.

</dd> <dt>

**szUserName**
</dt> <dd>

Nome utente utilizzato per l'autenticazione con il server proxy oppure stringa vuota se non è necessaria alcuna autenticazione.

WUA non usa questi dati se **szProxyAddr** è vuoto.

</dd> <dt>

**szPassword**
</dt> <dd>

Password utilizzata per l'autenticazione con il server proxy oppure stringa vuota se non è necessaria alcuna autenticazione.

WUA non usa questi dati se **szProxyAddr** è vuoto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




