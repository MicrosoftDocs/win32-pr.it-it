---
description: Definisce un algoritmo di crittografia per la crittografia e la decrittografia dei dati.
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: DOT11_CIPHER_ALGORITHM enumerazione (Wlantypes.h)
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
ms.openlocfilehash: c99ef5b648c5503743de6f51ce7d035d75dbe1f3e5593d473a374813f4000566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780241"
---
# <a name="dot11_cipher_algorithm-enumeration"></a>Enumerazione DOT11 \_ CIPHER \_ ALGORITHM

Il **tipo enumerato \_ DOT11 CIPHER \_ ALGORITHM** definisce un algoritmo di crittografia per la crittografia dei dati e la decrittografia.

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

<span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11 \_ CIPHER \_ ALGO \_ NONE**
</dt> <dd>

Specifica che nessun algoritmo di crittografia è abilitato o supportato.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11 \_ CIPHER \_ ALGO \_ WEP40**
</dt> <dd>

Specifica un algoritmo WEP (Wired Equivalent Privacy), ovvero l'algoritmo basato su RC4 specificato nello standard 802.11-1999. Questo enumeratore specifica l'algoritmo di crittografia WEP con una chiave di crittografia a 40 bit.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11 \_ CIPHER \_ ALGO \_ TKIP**
</dt> <dd>

Specifica un algoritmo TKIP (Temporal Key Integrity Protocol), ovvero la suite di crittografia basata su RC4 basata sugli algoritmi definiti nella specifica WPA e nello standard IEEE 802.11i-2004. Questa crittografia usa anche l'algoritmo Michael Message Integrity Code (MIC) per la protezione dalla falsificazione.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11 \_ CIPHER \_ ALGO \_ CCMP**
</dt> <dd>

Specifica un algoritmo AES-CCMP, come specificato nello standard IEEE 802.11i-2004 e rfc 3610. Advanced Encryption Standard (AES) è l'algoritmo di crittografia definito in FIPS PUB 197.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11 \_ CIPHER \_ ALGO \_ WEP104**
</dt> <dd>

Specifica un algoritmo di crittografia WEP con una chiave di crittografia a 104 bit.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11 \_ CIPHER \_ ALGO \_ WPA \_ USE \_ GROUP**
</dt> <dd>

Specifica una suite Wi-Fi di crittografia con chiave di gruppo per l'accesso protetto (WPA). Per altre informazioni sulla suite di crittografia Use Group Key, vedere la clausola 7.3.2.25.1 dello standard IEEE 802.11i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11 \_ CIPHER \_ ALGO \_ RSN \_ USE \_ GROUP**
</dt> <dd>

Specifica una suite di crittografia RSN (Robust Security Network) Use Group Key. Per altre informazioni sulla suite di crittografia Use Group Key, vedere la clausola 7.3.2.25.1 dello standard IEEE 802.11i-2004.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11 \_ CIPHER \_ ALGO \_ WEP**
</dt> <dd>

Specifica un algoritmo di crittografia WEP con una chiave di crittografia di qualsiasi lunghezza.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11 \_ CIPHER \_ ALGO \_ IHV \_ START**
</dt> <dd>

Specifica l'inizio dell'intervallo utilizzato per definire algoritmi di crittografia proprietari sviluppati da un fornitore di hardware indipendente (IHV).

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11 \_ CIPHER \_ ALGO \_ IHV \_ END**
</dt> <dd>

Specifica la fine dell'intervallo utilizzato per definire algoritmi di crittografia proprietari sviluppati da un IHV.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                        |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Wlantypes.h (include Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COPPIA DI CRITTOGRAFIA \_ \_ DELL'AUTENTICAZIONE DOT11 \_**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**RETE DISPONIBILE \_ \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**ATTRIBUTI DI \_ SICUREZZA \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




