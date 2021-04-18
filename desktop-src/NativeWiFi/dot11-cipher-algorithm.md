---
description: Definisce un algoritmo di crittografia per la crittografia e la decrittografia dei dati.
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: Enumerazione DOT11_CIPHER_ALGORITHM (wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_CIPHER_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fcbd61476458b5ed906ee57af6ab22b35f0378d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313763"
---
# <a name="dot11_cipher_algorithm-enumeration"></a>\_Enumerazione algoritmo di crittografia DOT11 \_

Il tipo enumerato **\_ \_ algoritmo di crittografia DOT11** definisce un algoritmo di crittografia per la crittografia e la decrittografia dei dati.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _DOT11_CIPHER_ALGORITHM { 
  DOT11_CIPHER_ALGO_NONE           = 0x00,
  DOT11_CIPHER_ALGO_WEP40          = 0x01,
  DOT11_CIPHER_ALGO_TKIP           = 0x02,
  DOT11_CIPHER_ALGO_CCMP           = 0x04,
  DOT11_CIPHER_ALGO_WEP104         = 0x05,
  DOT11_CIPHER_ALGO_WPA_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_RSN_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_WEP            = 0x101,
  DOT11_CIPHER_ALGO_IHV_START      = 0x80000000,
  DOT11_CIPHER_ALGO_IHV_END        = 0xffffffff
} DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**\_Algoritmo di crittografia DOT11 \_ \_ None**
</dt> <dd>

Specifica che non è abilitato né supportato alcun algoritmo di crittografia.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11 \_ crittografia \_ algo \_ WEP40**
</dt> <dd>

Specifica un algoritmo WEP (Wired equivalente privacy), che è l'algoritmo basato su RC4 specificato nello standard 802.11-1999. Questo enumeratore specifica l'algoritmo di crittografia WEP con una chiave di crittografia a 40 bit.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**\_Algoritmo crittografia \_ DOT11 \_**
</dt> <dd>

Specifica un algoritmo TKIP (Temporal Key Integrity Protocol), ovvero il pacchetto di crittografia basato su RC4 basato sugli algoritmi definiti nella specifica WPA e nello standard IEEE 802.11 i-2004. Questa crittografia usa anche l'algoritmo MIC (Message Integrity Code) di Michael per la protezione da falsificazione.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**\_Algoritmo di crittografia DOT11 \_ \_**
</dt> <dd>

Specifica un algoritmo AES-CCMP, come specificato nello standard IEEE 802.11 i-2004 e RFC 3610. Advanced Encryption Standard (AES) è l'algoritmo di crittografia definito in FIPS PUB 197.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11 \_ crittografia \_ algo \_ WEP104**
</dt> <dd>

Specifica un algoritmo di crittografia WEP con una chiave di crittografia a 104 bit.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11 \_ crittografia \_ algoritmo \_ WPA \_ utilizzo \_ gruppo**
</dt> <dd>

Specifica un Wi-Fi di accesso protetto (WPA) utilizzando il gruppo di crittografia della chiave del gruppo. Per ulteriori informazioni sull'utilizzo del pacchetto di crittografia della chiave del gruppo, vedere la clausola 7.3.2.25.1 dello standard IEEE 802.11 i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11 \_ crittografia \_ algo \_ RSN \_ utilizzo \_ gruppo**
</dt> <dd>

Specifica una rete di sicurezza robusta (RSN) che utilizza il pacchetto di crittografia con chiave del gruppo. Per ulteriori informazioni sull'utilizzo del pacchetto di crittografia della chiave del gruppo, vedere la clausola 7.3.2.25.1 dello standard IEEE 802.11 i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11 \_ crittografia \_ algoritmo \_ WEP**
</dt> <dd>

Specifica un algoritmo di crittografia WEP con una chiave di crittografia di qualsiasi lunghezza.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11 \_ crittografia \_ algo \_ IHV \_ Start**
</dt> <dd>

Specifica l'inizio dell'intervallo utilizzato per definire algoritmi di crittografia proprietari sviluppati da un fornitore di hardware indipendente (IHV).

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11 \_ crittografia \_ algo \_ IHV \_ end**
</dt> <dd>

Specifica la fine dell'intervallo utilizzata per definire algoritmi di crittografia proprietari sviluppati da un IHV.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                        |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Wlantypes. h (include Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Coppia di \_ crittografia \_ AUTH DOT11**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**\_rete disponibile \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**\_attributi di sicurezza WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




