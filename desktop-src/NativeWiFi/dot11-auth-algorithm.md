---
description: Definisce un algoritmo di autenticazione LAN wireless.
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: Enumerazione DOT11_AUTH_ALGORITHM (wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 1b14886c62448194b79eab2e0302ce5608ad282d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313768"
---
# <a name="dot11_auth_algorithm-enumeration"></a>Enumerazione dell'algoritmo di \_ autenticazione DOT11 \_

Il tipo enumerato **\_ \_ algoritmo** di autenticazione DOT11 definisce un algoritmo di autenticazione LAN wireless.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _DOT11_AUTH_ALGORITHM { 
  DOT11_AUTH_ALGO_80211_OPEN        = 1,
  DOT11_AUTH_ALGO_80211_SHARED_KEY  = 2,
  DOT11_AUTH_ALGO_WPA               = 3,
  DOT11_AUTH_ALGO_WPA_PSK           = 4,
  DOT11_AUTH_ALGO_WPA_NONE          = 5,
  DOT11_AUTH_ALGO_RSNA              = 6,
  DOT11_AUTH_ALGO_RSNA_PSK          = 7,
  DOT11_AUTH_ALGO_IHV_START         = 0x80000000,
  DOT11_AUTH_ALGO_IHV_END           = 0xffffffff
} DOT11_AUTH_ALGORITHM, *PDOT11_AUTH_ALGORITHM;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11 \_ AUTH \_ \_ 80211 \_ Open**
</dt> <dd>

Specifica un algoritmo di autenticazione di sistema aperto IEEE 802,11.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**\_ \_ \_ Chiave condivisa algo 80211 \_ \_ di DOT11 auth**
</dt> <dd>

Specifica un algoritmo di autenticazione con chiave condivisa 802,11 che richiede l'uso di una chiave di privacy equivalente cablata (WEP) pre-condivisa per l'autenticazione di 802,11.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11 \_ auth \_ algo \_ WPA**
</dt> <dd>

Specifica un algoritmo WPA (Wi-Fi Protected Access). L'autenticazione della porta IEEE 802.1 X viene eseguita dal richiedente, dall'autenticatore e dal server di autenticazione. Le chiavi di crittografia vengono derivate dinamicamente tramite il processo di autenticazione.

Questo algoritmo è valido solo per i tipi BSS dell'infrastruttura dei tipi dot11 \_ BSS \_ \_ .

Quando l'algoritmo WPA è abilitato, la stazione 802,11 verrà associata solo a un punto di accesso le cui risposte beacon o Probe contengono la suite di autenticazione di tipo 1 (802.1 X) all'interno dell'elemento informazioni WPA (IE).

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11 \_ auth \_ algo \_ WPA \_ PSK**
</dt> <dd>

Specifica un algoritmo WPA che usa chiavi precondivise (PSK). L'autenticazione della porta IEEE 802.1 X viene eseguita dal supplicant e dall'autenticatore. Le chiavi di crittografia vengono derivate in modo dinamico tramite una chiave precondivisa utilizzata sia nel supplicant che nell'autenticatore.

Questo algoritmo è valido solo per i tipi BSS **dell' \_ \_ \_ infrastruttura dei tipi dot11 BSS**.

Quando è abilitato l'algoritmo WPA PSK, la stazione 802,11 verrà associata solo a un punto di accesso le cui risposte di Beacon o Probe contengono la suite di autenticazione di tipo 2 (chiave precondivisa) all'interno dell'IE WPA.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11 \_ auth \_ algo \_ \_**
</dt> <dd>

Questo valore non è supportato.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**\_RSNA di autenticazione DOT11 \_ algo \_**
</dt> <dd>

Specifica un algoritmo di associazione alla rete di sicurezza (RSNA) 802.11 i robusti. WPA2 è un algoritmo di questo tipo. L'autenticazione della porta IEEE 802.1 X viene eseguita dal richiedente, dall'autenticatore e dal server di autenticazione. Le chiavi di crittografia vengono derivate dinamicamente tramite il processo di autenticazione.

Questo algoritmo è valido solo per i tipi BSS **dell' \_ \_ \_ infrastruttura dei tipi dot11 BSS**.

Quando l'algoritmo RSNA è abilitato, la stazione 802,11 verrà associata solo a un punto di accesso le cui risposte beacon o Probe contengono la suite di autenticazione di tipo 1 (802.1 X) all'interno di RSN IE.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11 \_ autenticazione \_ algo \_ RSNA \_ PSK**
</dt> <dd>

Specifica un algoritmo 802.11 i RSNA che usa PSK. L'autenticazione della porta IEEE 802.1 X viene eseguita dal supplicant e dall'autenticatore. Le chiavi di crittografia vengono derivate in modo dinamico tramite una chiave precondivisa utilizzata sia nel supplicant che nell'autenticatore.

Questo algoritmo è valido solo per i tipi BSS **dell' \_ \_ \_ infrastruttura dei tipi dot11 BSS**.

Quando l'algoritmo RSNA PSK è abilitato, la stazione 802,11 verrà associata solo a un punto di accesso le cui risposte beacon o Probe contengono la suite di autenticazione di tipo 2 (chiave precondivisa) all'interno di RSN IE.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**Avvio di DOT11 \_ auth \_ \_ IHV \_**
</dt> <dd>

Indica l'inizio dell'intervallo che specifica gli algoritmi di autenticazione proprietari sviluppati da un IHV.

**DOT11 \_ auth \_ \_ IHV \_ Start** Enumerator è valido solo quando il driver miniport funziona in modalità Extensible Station (ExtSTA).

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11 \_ Authentication \_ algo \_ IHV \_ end**
</dt> <dd>

Indica la fine dell'intervallo che specifica gli algoritmi di autenticazione proprietari sviluppati da un IHV.

L'enumeratore **end di DOT11 \_ auth \_ \_ IHV \_** è valido solo quando il driver miniport funziona in modalità ExtSTA.

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

 

 




