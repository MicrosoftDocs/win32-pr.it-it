---
description: Contiene le credenziali di accesso per una connessione.
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: Elemento UserLogonCred (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129563"
---
# <a name="userlogoncred-contexttype-element"></a>Elemento UserLogonCred (contextType)

L'elemento **UserLogonCred (ContextType)** contiene le credenziali di accesso per una connessione.

Questo elemento può avere gli elementi figlio seguenti.

-   [**Nome utente**](schema-username-userlogoncred-element.md)
-   [**Password**](schema-password-userlogoncred-element.md)
-   [**IgnorePassword**](schema-ignorepassword-userlogoncred-element.md)

Questo elemento può avere un massimo di un'occorrenza.

Questo elemento è facoltativo.

``` syntax
<xs:element name="UserLogonCred">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="UserName"
                type="nameType"
             />
            <xs:element name="IgnorePassword"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="Password"
                type="string"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L'elemento **UserLogonCred** è definito dal tipo complesso [**contextType**](schema-contexttype-complextype.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Tipo                                           | Descrizione                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [**IgnorePassword**](schema-ignorepassword-userlogoncred-element.md) | boolean                                        | Come gestire le password durante l'aggiornamento dei profili.<br/> |
| [**Password**](schema-password-userlogoncred-element.md)             | string                                         | Password utente.<br/>                                   |
| [**Nome utente**](schema-username-userlogoncred-element.md)             | [**nameType**](schema-nametype-simpletype.md) | Nome utente.<br/>                                       |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**Contesto (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




