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
# <a name="dot11_cipher_algorithm-enumeration"></a><span data-ttu-id="b8be6-103">\_Enumerazione algoritmo di crittografia DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="b8be6-103">DOT11\_CIPHER\_ALGORITHM enumeration</span></span>

<span data-ttu-id="b8be6-104">Il tipo enumerato **\_ \_ algoritmo di crittografia DOT11** definisce un algoritmo di crittografia per la crittografia e la decrittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="b8be6-104">The **DOT11\_CIPHER\_ALGORITHM** enumerated type defines a cipher algorithm for data encryption and decryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8be6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8be6-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="b8be6-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="b8be6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b8be6-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**\_Algoritmo di crittografia DOT11 \_ \_ None**</span><span class="sxs-lookup"><span data-stu-id="b8be6-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11\_CIPHER\_ALGO\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="b8be6-108">Specifica che non è abilitato né supportato alcun algoritmo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="b8be6-108">Specifies that no cipher algorithm is enabled or supported.</span></span>

</dd> <dt>

<span data-ttu-id="b8be6-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11 \_ crittografia \_ algo \_ WEP40**</span><span class="sxs-lookup"><span data-stu-id="b8be6-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11\_CIPHER\_ALGO\_WEP40**</span></span>
</dt> <dd>

<span data-ttu-id="b8be6-110">Specifica un algoritmo WEP (Wired equivalente privacy), che è l'algoritmo basato su RC4 specificato nello standard 802.11-1999.</span><span class="sxs-lookup"><span data-stu-id="b8be6-110">Specifies a Wired Equivalent Privacy (WEP) algorithm, which is the RC4-based algorithm that is specified in the 802.11-1999 standard.</span></span> <span data-ttu-id="b8be6-111">Questo enumeratore specifica l'algoritmo di crittografia WEP con una chiave di crittografia a 40 bit.</span><span class="sxs-lookup"><span data-stu-id="b8be6-111">This enumerator specifies the WEP cipher algorithm with a 40-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="b8be6-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**\_Algoritmo crittografia \_ DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="b8be6-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11\_CIPHER\_ALGO\_TKIP**</span></span>
</dt> <dd>

<span data-ttu-id="b8be6-113">Specifica un algoritmo TKIP (Temporal Key Integrity Protocol), ovvero il pacchetto di crittografia basato su RC4 basato sugli algoritmi definiti nella specifica WPA e nello standard IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="b8be6-113">Specifies a Temporal Key Integrity Protocol (TKIP) algorithm, which is the RC4-based cipher suite that is based on the algorithms that are defined in the WPA specification and IEEE 802.11i-2004 standard.</span></span> <span data-ttu-id="b8be6-114">Questa crittografia usa anche l'algoritmo MIC (Message Integrity Code) di Michael per la protezione da falsificazione.</span><span class="sxs-lookup"><span data-stu-id="b8be6-114">This cipher also uses the Michael Message Integrity Code (MIC) algorithm for forgery protection.</span></span>

</dd> <dt>

<span data-ttu-id="b8be6-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**\_Algoritmo di crittografia DOT11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b8be6-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11\_CIPHER\_ALGO\_CCMP**</span></span>
</dt> <dd>

<span data-ttu-id="b8be6-116">Specifica un algoritmo AES-CCMP, come specificato nello standard IEEE 802.11 i-2004 e RFC 3610.</span><span class="sxs-lookup"><span data-stu-id="b8be6-116">Specifies an AES-CCMP algorithm, as specified in the IEEE 802.11i-2004 standard and RFC 3610.</span></span> <span data-ttu-id="b8be6-117">Advanced Encryption Standard (AES) è l'algoritmo di crittografia definito in FIPS PUB 197.</span><span class="sxs-lookup"><span data-stu-id="b8be6-117">Advanced Encryption Standard (AES) is the encryption algorithm defined in FIPS PUB 197.</span></span>

</dd> <dt>

<span data-ttu-id="b8be6-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11 \_ crittografia \_ algo \_ WEP104**</span><span class="sxs-lookup"><span data-stu-id="b8be6-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11\_CIPHER\_ALGO\_WEP104**</span></span>
</dt> <dd>

<span data-ttu-id="b8be6-119">Specifica un algoritmo di crittografia WEP con una chiave di crittografia a 104 bit.</span><span class="sxs-lookup"><span data-stu-id="b8be6-119">Specifies a WEP cipher algorithm with a 104-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="b8be6-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11 \_ crittografia \_ algoritmo \_ WPA \_ utilizzo \_ gruppo**</span><span class="sxs-lookup"><span data-stu-id="b8be6-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11\_CIPHER\_ALGO\_WPA\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="b8be6-121">Specifica un Wi-Fi di accesso protetto (WPA) utilizzando il gruppo di crittografia della chiave del gruppo.</span><span class="sxs-lookup"><span data-stu-id="b8be6-121">Specifies a Wi-Fi Protected Access (WPA) Use Group Key cipher suite.</span></span> <span data-ttu-id="b8be6-122">Per ulteriori informazioni sull'utilizzo del pacchetto di crittografia della chiave del gruppo, vedere la clausola 7.3.2.25.1 dello standard IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="b8be6-122">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="b8be6-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11 \_ crittografia \_ algo \_ RSN \_ utilizzo \_ gruppo**</span><span class="sxs-lookup"><span data-stu-id="b8be6-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11\_CIPHER\_ALGO\_RSN\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="b8be6-124">Specifica una rete di sicurezza robusta (RSN) che utilizza il pacchetto di crittografia con chiave del gruppo.</span><span class="sxs-lookup"><span data-stu-id="b8be6-124">Specifies a Robust Security Network (RSN) Use Group Key cipher suite.</span></span> <span data-ttu-id="b8be6-125">Per ulteriori informazioni sull'utilizzo del pacchetto di crittografia della chiave del gruppo, vedere la clausola 7.3.2.25.1 dello standard IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="b8be6-125">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="b8be6-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11 \_ crittografia \_ algoritmo \_ WEP**</span><span class="sxs-lookup"><span data-stu-id="b8be6-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11\_CIPHER\_ALGO\_WEP**</span></span>
</dt> <dd>

<span data-ttu-id="b8be6-127">Specifica un algoritmo di crittografia WEP con una chiave di crittografia di qualsiasi lunghezza.</span><span class="sxs-lookup"><span data-stu-id="b8be6-127">Specifies a WEP cipher algorithm with a cipher key of any length.</span></span>

</dd> <dt>

<span data-ttu-id="b8be6-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11 \_ crittografia \_ algo \_ IHV \_ Start**</span><span class="sxs-lookup"><span data-stu-id="b8be6-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11\_CIPHER\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="b8be6-129">Specifica l'inizio dell'intervallo utilizzato per definire algoritmi di crittografia proprietari sviluppati da un fornitore di hardware indipendente (IHV).</span><span class="sxs-lookup"><span data-stu-id="b8be6-129">Specifies the start of the range that is used to define proprietary cipher algorithms that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="b8be6-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11 \_ crittografia \_ algo \_ IHV \_ end**</span><span class="sxs-lookup"><span data-stu-id="b8be6-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11\_CIPHER\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="b8be6-131">Specifica la fine dell'intervallo utilizzata per definire algoritmi di crittografia proprietari sviluppati da un IHV.</span><span class="sxs-lookup"><span data-stu-id="b8be6-131">Specifies the end of the range that is used to define proprietary cipher algorithms that are developed by an IHV.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8be6-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8be6-132">Requirements</span></span>



| <span data-ttu-id="b8be6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8be6-133">Requirement</span></span> | <span data-ttu-id="b8be6-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b8be6-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8be6-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8be6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b8be6-136">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="b8be6-136">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b8be6-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8be6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b8be6-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8be6-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="b8be6-139">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b8be6-139">Redistributable</span></span><br/>          | <span data-ttu-id="b8be6-140">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="b8be6-140">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="b8be6-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8be6-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8be6-142"><dt>Wlantypes. h (include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8be6-142"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8be6-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8be6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8be6-144">**\_Coppia di \_ crittografia \_ AUTH DOT11**</span><span class="sxs-lookup"><span data-stu-id="b8be6-144">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="b8be6-145">**\_rete disponibile \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="b8be6-145">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="b8be6-146">**\_attributi di sicurezza WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="b8be6-146">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




