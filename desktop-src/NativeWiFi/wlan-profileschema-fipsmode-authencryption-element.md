---
description: Indica se la modalità FIPS (Federal Information Processing Standards) è abilitata.
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: Elemento FIPSMode (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752303"
---
# <a name="fipsmode-authencryption-element"></a>Elemento FIPSMode (authEncryption)

L'elemento **FIPSMode** (authEncryption) indica se la modalità FIPS (Federal Information Processing Standards) è abilitata. Quando una connessione wireless funziona in modalità FIPS, il livello di sicurezza della connessione è conforme allo standard FIPS 140-2. Per ulteriori informazioni su FIPS, vedere la [Home page di FIPS](https://www.itl.nist.gov/fipspubs/).

Questo elemento è facoltativo. Se questo elemento non viene specificato in un profilo, la modalità FIPS non è abilitata.

**FIPSMode** può essere impostato su true solo quando vengono soddisfatte le condizioni seguenti:

-   L'elemento [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) ha un valore `ESS` (ovvero la connessione è una connessione di infrastruttura).
-   Il valore dell'elemento [**Authentication**](wlan-profileschema-authentication-authencryption-element.md) è `WPA2` o `WPA2PSK` .
-   Il valore dell'elemento [**Encryption**](wlan-profileschema-encryption-authencryption-element.md) è `AES` .

A differenza della maggior parte degli elementi nello \_ schema del profilo WLAN, questo elemento si trova nello `https://www.microsoft.com/networking/WLAN/profile/v2` spazio dei nomi.

Il valore dell'elemento **FIPSMode** viene ignorato se il driver miniport per l'interfaccia wireless non supporta la modalità FIPS.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato. Se **FIPSMode** è presente in un profilo, l'elemento viene ignorato.

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

L'elemento è definito dall'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Commenti

Questo parametro può essere impostato dalla riga di comando tramite il comando **netsh wlan set profileparameter** . Per ulteriori informazioni, vedere [comandi Netsh per WLAN (wireless local area network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="examples"></a>Esempio

Per visualizzare un profilo di esempio che usa l'elemento **FIPSMode** , vedere [esempio di profilo FIPS](fips-profile-sample.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



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

 

 
