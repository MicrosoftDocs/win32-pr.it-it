---
description: Indica se viene utilizzata l'autenticazione 802.1 X.
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
ms.openlocfilehash: cb327be4006e8da0074815a74e49d3ccdc5d3c84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313760"
---
# <a name="useonex-authencryption-element"></a>Elemento useOneX (authEncryption)

L'elemento useOneX (authEncryption) indica se viene utilizzata l'autenticazione 802.1 X.

``` syntax
<xs:element name="useOneX"
    type="boolean"
    minOccurs="0"
 />
```

L'elemento è definito dall'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **useOneX** , vedere esempi di profili [wireless](wireless-profile-samples.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                |
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

 

 




