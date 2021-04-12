---
description: Contiene una chiave di rete o una passphrase.
ms.assetid: d2ed407e-5eaa-477b-8c4d-a47795048e0b
title: Elemento portamateriali (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyMaterial
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 59f3fc25fda5f4bf4221417636ac25ab7d0f9a15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231725"
---
# <a name="keymaterial-sharedkey-element"></a>Elemento portamateriali (sharedKey)

L'elemento sharedKey contiene una chiave di rete o una passphrase. Se il valore dell'elemento [**protected**](wlan-profileschema-protected-sharedkey-element.md) è true, il materiale della chiave verrà crittografato. in caso contrario, il materiale della chiave non è crittografato. Il materiale della chiave crittografata è espresso in formato esadecimale.

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

L'elemento è definito dall'elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Commenti

L'intervallo di valori validi per l'elemento del materiale di crittografia varia in base al tipo di autenticazione e crittografia utilizzato, come specificato dagli elementi [**Authentication**](wlan-profileschema-authentication-authencryption-element.md) e [**Encryption**](wlan-profileschema-encryption-authencryption-element.md) . Varia anche in base al [**tipo di tipo**](wlan-profileschema-keytype-sharedkey-element.md).

Nella tabella seguente vengono illustrati i valori validi del **materiale** per alcune coppie di autenticazione e di crittografia.



| valore di [**autenticazione**](wlan-profileschema-authentication-authencryption-element.md) | valore di [**crittografia**](wlan-profileschema-encryption-authencryption-element.md) | valore di [**tipo di tipo**](wlan-profileschema-keytype-sharedkey-element.md) | Valori validi per il **materiale** consentiti                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| aperto o condiviso                                                                           | WEP                                                                              | networkKey                                                            | Questo elemento contiene una chiave WEP di 5 o 13 caratteri ANSI oppure di 10 o 26 caratteri esadecimali.                                                                                             |
| WPAPSK o WPA2PSK                                                                        | TKIP o AES                                                                      | passPhrase                                                            | Questo elemento contiene una passphrase da 8 a 63 caratteri ASCII, ovvero da 8 a 63 caratteri ANSI nell'intervallo da 32 a 126. I valori di chiave devono essere conformi ai requisiti specificati da 802.11 i. |
| WPAPSK o WPA2PSK                                                                        | TKIP o AES                                                                      | networkKey                                                            | Questo elemento contiene una chiave di 64 caratteri esadecimali.                                                                                                                                      |



 

È possibile immettere caratteri Unicode in cui vengono specificati i caratteri ANSI o ASCII. Tuttavia, se non è possibile eseguire il mapping dei caratteri Unicode specificati ai caratteri ANSI o ASCII, il materiale della chiave fornito viene rifiutato.

Il materiale della chiave restituito da [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) è sempre crittografato. Inoltre, se il materiale della chiave non crittografata viene passato a [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), il materiale della chiave viene crittografato automaticamente prima di essere archiviato nell'archivio profili.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il materiale della chiave non viene mai crittografato.

Se il processo viene eseguito nel contesto dell'account LocalSystem, è possibile decrittografare il materiale della chiave chiamando [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **codematerial** , vedere esempio di profilo [non broadcast](non-broadcast-profile-sample.md), esempio di [profilo WPA-Personal](wpa-personal-profile-sample.md)e [esempio di profilo WPA2-Personal](wpa2-personal-profile-sample.md).

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

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**sharedKey (sicurezza)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 
