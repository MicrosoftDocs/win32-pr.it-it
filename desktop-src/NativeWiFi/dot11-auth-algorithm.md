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
# <a name="dot11_auth_algorithm-enumeration"></a><span data-ttu-id="ed58b-103">Enumerazione dell'algoritmo di \_ autenticazione DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="ed58b-103">DOT11\_AUTH\_ALGORITHM enumeration</span></span>

<span data-ttu-id="ed58b-104">Il tipo enumerato **\_ \_ algoritmo** di autenticazione DOT11 definisce un algoritmo di autenticazione LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="ed58b-104">The **DOT11\_AUTH\_ALGORITHM** enumerated type defines a wireless LAN authentication algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed58b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed58b-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="ed58b-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="ed58b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ed58b-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11 \_ AUTH \_ \_ 80211 \_ Open**</span><span class="sxs-lookup"><span data-stu-id="ed58b-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11\_AUTH\_ALGO\_80211\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="ed58b-108">Specifica un algoritmo di autenticazione di sistema aperto IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="ed58b-108">Specifies an IEEE 802.11 Open System authentication algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="ed58b-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**\_ \_ \_ Chiave condivisa algo 80211 \_ \_ di DOT11 auth**</span><span class="sxs-lookup"><span data-stu-id="ed58b-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11\_AUTH\_ALGO\_80211\_SHARED\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="ed58b-110">Specifica un algoritmo di autenticazione con chiave condivisa 802,11 che richiede l'uso di una chiave di privacy equivalente cablata (WEP) pre-condivisa per l'autenticazione di 802,11.</span><span class="sxs-lookup"><span data-stu-id="ed58b-110">Specifies an 802.11 Shared Key authentication algorithm that requires the use of a pre-shared Wired Equivalent Privacy (WEP) key for the 802.11 authentication.</span></span>

</dd> <dt>

<span data-ttu-id="ed58b-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11 \_ auth \_ algo \_ WPA**</span><span class="sxs-lookup"><span data-stu-id="ed58b-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11\_AUTH\_ALGO\_WPA**</span></span>
</dt> <dd>

<span data-ttu-id="ed58b-112">Specifica un algoritmo WPA (Wi-Fi Protected Access).</span><span class="sxs-lookup"><span data-stu-id="ed58b-112">Specifies a Wi-Fi Protected Access (WPA) algorithm.</span></span> <span data-ttu-id="ed58b-113">L'autenticazione della porta IEEE 802.1 X viene eseguita dal richiedente, dall'autenticatore e dal server di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ed58b-113">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="ed58b-114">Le chiavi di crittografia vengono derivate dinamicamente tramite il processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ed58b-114">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="ed58b-115">Questo algoritmo è valido solo per i tipi BSS dell'infrastruttura dei tipi dot11 \_ BSS \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ed58b-115">This algorithm is valid only for BSS types of dot11\_BSS\_type\_infrastructure.</span></span>

<span data-ttu-id="ed58b-116">Quando l'algoritmo WPA è abilitato, la stazione 802,11 verrà associata solo a un punto di accesso le cui risposte beacon o Probe contengono la suite di autenticazione di tipo 1 (802.1 X) all'interno dell'elemento informazioni WPA (IE).</span><span class="sxs-lookup"><span data-stu-id="ed58b-116">When the WPA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the WPA information element (IE).</span></span>

</dd> <dt>

<span data-ttu-id="ed58b-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11 \_ auth \_ algo \_ WPA \_ PSK**</span><span class="sxs-lookup"><span data-stu-id="ed58b-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11\_AUTH\_ALGO\_WPA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="ed58b-118">Specifica un algoritmo WPA che usa chiavi precondivise (PSK).</span><span class="sxs-lookup"><span data-stu-id="ed58b-118">Specifies a WPA algorithm that uses preshared keys (PSK).</span></span> <span data-ttu-id="ed58b-119">L'autenticazione della porta IEEE 802.1 X viene eseguita dal supplicant e dall'autenticatore.</span><span class="sxs-lookup"><span data-stu-id="ed58b-119">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="ed58b-120">Le chiavi di crittografia vengono derivate in modo dinamico tramite una chiave precondivisa utilizzata sia nel supplicant che nell'autenticatore.</span><span class="sxs-lookup"><span data-stu-id="ed58b-120">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="ed58b-121">Questo algoritmo è valido solo per i tipi BSS **dell' \_ \_ \_ infrastruttura dei tipi dot11 BSS**.</span><span class="sxs-lookup"><span data-stu-id="ed58b-121">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="ed58b-122">Quando è abilitato l'algoritmo WPA PSK, la stazione 802,11 verrà associata solo a un punto di accesso le cui risposte di Beacon o Probe contengono la suite di autenticazione di tipo 2 (chiave precondivisa) all'interno dell'IE WPA.</span><span class="sxs-lookup"><span data-stu-id="ed58b-122">When the WPA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2 (preshared key) within the WPA IE.</span></span>

</dd> <dt>

<span data-ttu-id="ed58b-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11 \_ auth \_ algo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed58b-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11\_AUTH\_ALGO\_WPA\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="ed58b-124">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ed58b-124">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ed58b-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**\_RSNA di autenticazione DOT11 \_ algo \_**</span><span class="sxs-lookup"><span data-stu-id="ed58b-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11\_AUTH\_ALGO\_RSNA**</span></span>
</dt> <dd>

<span data-ttu-id="ed58b-126">Specifica un algoritmo di associazione alla rete di sicurezza (RSNA) 802.11 i robusti.</span><span class="sxs-lookup"><span data-stu-id="ed58b-126">Specifies an 802.11i Robust Security Network Association (RSNA) algorithm.</span></span> <span data-ttu-id="ed58b-127">WPA2 è un algoritmo di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="ed58b-127">WPA2 is one such algorithm.</span></span> <span data-ttu-id="ed58b-128">L'autenticazione della porta IEEE 802.1 X viene eseguita dal richiedente, dall'autenticatore e dal server di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ed58b-128">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="ed58b-129">Le chiavi di crittografia vengono derivate dinamicamente tramite il processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ed58b-129">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="ed58b-130">Questo algoritmo è valido solo per i tipi BSS **dell' \_ \_ \_ infrastruttura dei tipi dot11 BSS**.</span><span class="sxs-lookup"><span data-stu-id="ed58b-130">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="ed58b-131">Quando l'algoritmo RSNA è abilitato, la stazione 802,11 verrà associata solo a un punto di accesso le cui risposte beacon o Probe contengono la suite di autenticazione di tipo 1 (802.1 X) all'interno di RSN IE.</span><span class="sxs-lookup"><span data-stu-id="ed58b-131">When the RSNA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="ed58b-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11 \_ autenticazione \_ algo \_ RSNA \_ PSK**</span><span class="sxs-lookup"><span data-stu-id="ed58b-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11\_AUTH\_ALGO\_RSNA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="ed58b-133">Specifica un algoritmo 802.11 i RSNA che usa PSK.</span><span class="sxs-lookup"><span data-stu-id="ed58b-133">Specifies an 802.11i RSNA algorithm that uses PSK.</span></span> <span data-ttu-id="ed58b-134">L'autenticazione della porta IEEE 802.1 X viene eseguita dal supplicant e dall'autenticatore.</span><span class="sxs-lookup"><span data-stu-id="ed58b-134">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="ed58b-135">Le chiavi di crittografia vengono derivate in modo dinamico tramite una chiave precondivisa utilizzata sia nel supplicant che nell'autenticatore.</span><span class="sxs-lookup"><span data-stu-id="ed58b-135">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="ed58b-136">Questo algoritmo è valido solo per i tipi BSS **dell' \_ \_ \_ infrastruttura dei tipi dot11 BSS**.</span><span class="sxs-lookup"><span data-stu-id="ed58b-136">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="ed58b-137">Quando l'algoritmo RSNA PSK è abilitato, la stazione 802,11 verrà associata solo a un punto di accesso le cui risposte beacon o Probe contengono la suite di autenticazione di tipo 2 (chiave precondivisa) all'interno di RSN IE.</span><span class="sxs-lookup"><span data-stu-id="ed58b-137">When the RSNA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2(preshared key) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="ed58b-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**Avvio di DOT11 \_ auth \_ \_ IHV \_**</span><span class="sxs-lookup"><span data-stu-id="ed58b-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11\_AUTH\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="ed58b-139">Indica l'inizio dell'intervallo che specifica gli algoritmi di autenticazione proprietari sviluppati da un IHV.</span><span class="sxs-lookup"><span data-stu-id="ed58b-139">Indicates the start of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="ed58b-140">**DOT11 \_ auth \_ \_ IHV \_ Start** Enumerator è valido solo quando il driver miniport funziona in modalità Extensible Station (ExtSTA).</span><span class="sxs-lookup"><span data-stu-id="ed58b-140">The **DOT11\_AUTH\_ALGO\_IHV\_START** enumerator is valid only when the miniport driver is operating in Extensible Station (ExtSTA) mode.</span></span>

</dd> <dt>

<span data-ttu-id="ed58b-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11 \_ Authentication \_ algo \_ IHV \_ end**</span><span class="sxs-lookup"><span data-stu-id="ed58b-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11\_AUTH\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="ed58b-142">Indica la fine dell'intervallo che specifica gli algoritmi di autenticazione proprietari sviluppati da un IHV.</span><span class="sxs-lookup"><span data-stu-id="ed58b-142">Indicates the end of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="ed58b-143">L'enumeratore **end di DOT11 \_ auth \_ \_ IHV \_** è valido solo quando il driver miniport funziona in modalità ExtSTA.</span><span class="sxs-lookup"><span data-stu-id="ed58b-143">The **DOT11\_AUTH\_ALGO\_IHV\_END** enumerator is valid only when the miniport driver is operating in ExtSTA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed58b-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed58b-144">Requirements</span></span>



| <span data-ttu-id="ed58b-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed58b-145">Requirement</span></span> | <span data-ttu-id="ed58b-146">Valore</span><span class="sxs-lookup"><span data-stu-id="ed58b-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed58b-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed58b-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ed58b-148">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="ed58b-148">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ed58b-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed58b-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ed58b-150">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ed58b-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="ed58b-151">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ed58b-151">Redistributable</span></span><br/>          | <span data-ttu-id="ed58b-152">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="ed58b-152">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="ed58b-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed58b-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed58b-154"><dt>Wlantypes. h (include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed58b-154"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed58b-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed58b-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed58b-156">**\_Coppia di \_ crittografia \_ AUTH DOT11**</span><span class="sxs-lookup"><span data-stu-id="ed58b-156">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="ed58b-157">**\_rete disponibile \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="ed58b-157">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="ed58b-158">**\_attributi di sicurezza WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="ed58b-158">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




