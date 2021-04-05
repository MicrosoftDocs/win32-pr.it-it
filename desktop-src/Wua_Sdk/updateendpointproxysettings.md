---
description: La struttura UpdateEndpointProxySettings definisce le impostazioni proxy usate per la richiesta di un token.
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: Struttura UpdateEndpointProxySettings (UpdateEndpointAuth. h)
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
ms.openlocfilehash: aad6ad294baab37b7516152438dbc9fd05f7036a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049537"
---
# <a name="updateendpointproxysettings-structure"></a>Struttura UpdateEndpointProxySettings

La struttura **UpdateEndpointProxySettings** definisce le impostazioni proxy usate per la richiesta di un token.

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

Il nome DNS o l'indirizzo IP del server proxy da usare (ad esempio, "proxy.somecorp.com" o "192.168.0.4") o una stringa vuota se non è necessario usare un proxy.

</dd> <dt>

**szBypassList**
</dt> <dd>

Elenco di indirizzi host che devono ignorare il server proxy oppure una stringa vuota se tutti gli indirizzi host devono usare il server proxy

WUA non utilizza questi dati se **szProxyAddr** è vuoto.

</dd> <dt>

**szUserName**
</dt> <dd>

Nome utente utilizzato per l'autenticazione con il server proxy oppure stringa vuota se non è necessaria alcuna autenticazione.

WUA non utilizza questi dati se **szProxyAddr** è vuoto.

</dd> <dt>

**szPassword**
</dt> <dd>

Password utilizzata per l'autenticazione con il server proxy oppure stringa vuota se non è necessaria alcuna autenticazione.

WUA non utilizza questi dati se **szProxyAddr** è vuoto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




