---
description: Indica se viene usata l'autenticazione 802.1X.
ms.assetid: dbddaf5a-7574-4282-ab4d-f6f697ed94ab
title: Elemento useOneX (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 961f1b6be52da97ada2c230579ac281652a07fcbae67ac32d2399eb2968b1946
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912571"
---
# <a name="useonex-authencryption-element"></a>Elemento useOneX (authEncryption)

L'elemento useOneX (authEncryption) indica se viene usata l'autenticazione 802.1X.

``` syntax
<xs:element name="useOneX"
    type="boolean"
    minOccurs="0"
 />
```

L'elemento è definito [**dall'elemento authEncryption.**](wlan-profileschema-authencryption-security-element.md)

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano **l'elemento useOneX,** vedere [Esempi di profili wireless](wireless-profile-samples.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**authEncryption (sicurezza)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




