---
description: Definisce un algoritmo di autenticazione LAN wireless.
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: DOT11_AUTH_ALGORITHM enumerazione (Wlantypes.h)
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
ms.openlocfilehash: 774b2218a451f4cbaa85e6b77559c0d5761b0b132ebdf9d3f11c15ea6658e7bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798471"
---
# <a name="dot11_auth_algorithm-enumeration"></a>Enumerazione DOT11 \_ AUTH \_ ALGORITHM

Il **tipo enumerato DOT11 \_ AUTH \_ ALGORITHM** definisce un algoritmo di autenticazione LAN wireless.

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

<span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11 \_ AUTH \_ ALGO \_ 80211 \_ OPEN**
</dt> <dd>

Specifica un algoritmo di autenticazione Open System IEEE 802.11.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11 \_ AUTH \_ ALGO \_ 80211 \_ CHIAVE \_ CONDIVISA**
</dt> <dd>

Specifica un algoritmo di autenticazione con chiave condivisa 802.11 che richiede l'uso di una chiave WEP (Wired Equivalent Privacy) precondi condivisa per l'autenticazione 802.11.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA**
</dt> <dd>

Specifica un Wi-Fi di accesso protetto (WPA). L'autenticazione della porta IEEE 802.1X viene eseguita dal server di autenticazione, autenticatore e supplicante. Le chiavi di crittografia vengono derivate dinamicamente tramite il processo di autenticazione.

Questo algoritmo è valido solo per i tipi BSS dell'infrastruttura di tipo \_ dot11 \_ BSS. \_

Quando l'algoritmo WPA è abilitato, la stazione 802.11 verrà associata solo a un punto di accesso le cui risposte di tipo 1 (802.1X) contengono la suite di autenticazione di tipo 1 (802.1X) all'interno dell'elemento di informazioni WPA (IE).

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA \_ PSK**
</dt> <dd>

Specifica un algoritmo WPA che usa chiavi precondivise (PSK). L'autenticazione della porta IEEE 802.1X viene eseguita dal supplicante e dall'autenticatore. Le chiavi di crittografia vengono derivate dinamicamente tramite una chiave precondivisa usata sia nell'autenticatore che nel supplicante.

Questo algoritmo è valido solo per i tipi BSS **dell'infrastruttura di tipo \_ dot11 BSS \_ \_**.

Quando l'algoritmo WPA PSK è abilitato, la stazione 802.11 verrà associata solo a un punto di accesso le cui risposte di tipo 2 (chiave precondivisa) contengono le risposte del beacon o del probe all'interno di WPA IE.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA \_ NONE**
</dt> <dd>

Questo valore non è supportato.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11 \_ AUTH \_ ALGO \_ RSNA**
</dt> <dd>

Specifica un algoritmo RSNA (Robust Security Network Association) 802.11i. WPA2 è un algoritmo di questo tipo. L'autenticazione della porta IEEE 802.1X viene eseguita dal server di autenticazione, autenticatore e supplicante. Le chiavi di crittografia vengono derivate dinamicamente tramite il processo di autenticazione.

Questo algoritmo è valido solo per i tipi BSS **dell'infrastruttura di tipo \_ dot11 BSS \_ \_**.

Quando l'algoritmo RSNA è abilitato, la stazione 802.11 verrà associata solo a un punto di accesso le cui risposte di tipo 1 (802.1X) contengono la suite di autenticazione di tipo 1 (802.1X) all'interno di RSN IE.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11 \_ AUTH \_ ALGO \_ RSNA \_ PSK**
</dt> <dd>

Specifica un algoritmo RSNA 802.11i che usa PSK. L'autenticazione della porta IEEE 802.1X viene eseguita dal supplicante e dall'autenticatore. Le chiavi di crittografia vengono derivate dinamicamente tramite una chiave precondivisa usata sia nell'autenticatore che nel supplicante.

Questo algoritmo è valido solo per i tipi BSS **dell'infrastruttura di tipo \_ dot11 BSS \_ \_**.

Quando l'algoritmo RSNA PSK è abilitato, la stazione 802.11 verrà associata solo a un punto di accesso le cui risposte di tipo beacon o probe contengono la suite di autenticazione di tipo 2 (chiave precondivisa) all'interno di RSN IE.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11 \_ AUTH \_ ALGO \_ IHV \_ START**
</dt> <dd>

Indica l'inizio dell'intervallo che specifica gli algoritmi di autenticazione proprietari sviluppati da un IHV.

L'enumeratore **\_ DOT11 AUTH \_ ALGO \_ IHV \_ START** è valido solo quando il driver miniport funziona in modalità ExtSTA (Extensible Station).

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11 \_ AUTH \_ ALGO \_ IHV \_ END**
</dt> <dd>

Indica la fine dell'intervallo che specifica gli algoritmi di autenticazione proprietari sviluppati da un IHV.

L'enumeratore **\_ DOT11 AUTH \_ ALGO \_ IHV \_ END** è valido solo quando il driver miniport funziona in modalità ExtSTA.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                        |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Wlantypes.h (includere Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DOT11 \_ AUTH \_ CIPHER \_ PAIR**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**RETE DISPONIBILE \_ \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**ATTRIBUTI DI SICUREZZA \_ \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




