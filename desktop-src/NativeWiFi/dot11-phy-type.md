---
description: Definisce un PHY 802,11 e un tipo di supporto.
ms.assetid: f3804e57-c633-4288-9749-2b267b1353ae
title: Enumerazione DOT11_PHY_TYPE (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_PHY_TYPE
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 4e8fc4a1154b9f95fad5024607435861b9e98ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882681"
---
# <a name="dot11_phy_type-enumeration"></a><span data-ttu-id="4dad2-103">\_Enumerazione del \_ Tipo PHY DOT11</span><span class="sxs-lookup"><span data-stu-id="4dad2-103">DOT11\_PHY\_TYPE enumeration</span></span>

<span data-ttu-id="4dad2-104">L'enumerazione del **\_ \_ Tipo PHY DOT11** definisce un PHY 802,11 e un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="4dad2-104">The **DOT11\_PHY\_TYPE** enumeration defines an 802.11 PHY and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dad2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4dad2-105">Syntax</span></span>


```C++
typedef enum _DOT11_PHY_TYPE { 
  dot11_phy_type_unknown     = 0,
  dot11_phy_type_any         = 0,
  dot11_phy_type_fhss        = 1,
  dot11_phy_type_dsss        = 2,
  dot11_phy_type_irbaseband  = 3,
  dot11_phy_type_ofdm        = 4,
  dot11_phy_type_hrdsss      = 5,
  dot11_phy_type_erp         = 6,
  dot11_phy_type_ht          = 7,
  dot11_phy_type_vht         = 8,
  dot11_phy_type_IHV_start   = 0x80000000,
  dot11_phy_type_IHV_end     = 0xffffffff
} DOT11_PHY_TYPE, *PDOT11_PHY_TYPE;
```



## <a name="constants"></a><span data-ttu-id="4dad2-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="4dad2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4dad2-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**\_Tipo PHY \_ dot11 \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="4dad2-107"><span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**dot11\_phy\_type\_unknown**</span></span>
</dt> <dd>

<span data-ttu-id="4dad2-108">Specifica un tipo PHY sconosciuto o non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="4dad2-108">Specifies an unknown or uninitialized PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="4dad2-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11 \_ PHY \_ digitare \_ any**</span><span class="sxs-lookup"><span data-stu-id="4dad2-109"><span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11\_phy\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="4dad2-110">Specifica qualsiasi tipo di PHY.</span><span class="sxs-lookup"><span data-stu-id="4dad2-110">Specifies any PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="4dad2-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11 \_ di \_ Tipo PHY \_ FHSS**</span><span class="sxs-lookup"><span data-stu-id="4dad2-111"><span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11\_phy\_type\_fhss**</span></span>
</dt> <dd>

<span data-ttu-id="4dad2-112">Specifica un PHY FHSS (Frequency-Hopping Spread-Spectrum).</span><span class="sxs-lookup"><span data-stu-id="4dad2-112">Specifies a frequency-hopping spread-spectrum (FHSS) PHY.</span></span> <span data-ttu-id="4dad2-113">I dispositivi Bluetooth possono usare FHSS o un adattamento di FHSS.</span><span class="sxs-lookup"><span data-stu-id="4dad2-113">Bluetooth devices can use FHSS or an adaptation of FHSS.</span></span>

</dd> <dt>

<span data-ttu-id="4dad2-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11 \_ di \_ Tipo PHY \_ DSSS**</span><span class="sxs-lookup"><span data-stu-id="4dad2-114"><span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11\_phy\_type\_dsss**</span></span>
</dt> <dd>

<span data-ttu-id="4dad2-115">Specifica un tipo di PHY DSSS (Direct Sequence Spread Spectrum).</span><span class="sxs-lookup"><span data-stu-id="4dad2-115">Specifies a direct sequence spread spectrum (DSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="4dad2-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11 \_ di \_ Tipo PHY \_ irbaseband**</span><span class="sxs-lookup"><span data-stu-id="4dad2-116"><span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11\_phy\_type\_irbaseband**</span></span>
</dt> <dd>

<span data-ttu-id="4dad2-117">Specifica un tipo PHY a infrarossi (IR).</span><span class="sxs-lookup"><span data-stu-id="4dad2-117">Specifies an infrared (IR) baseband PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="4dad2-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**dot11 \_ di \_ Tipo PHY \_ OFDM**</span><span class="sxs-lookup"><span data-stu-id="4dad2-118"><span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**dot11\_phy\_type\_ofdm**</span></span>
</dt> <dd>

<span data-ttu-id="4dad2-119">Specifica un tipo PHY OFDM (ortogonal Frequency Division Multiplexing).</span><span class="sxs-lookup"><span data-stu-id="4dad2-119">Specifies an orthogonal frequency division multiplexing (OFDM) PHY type.</span></span> <span data-ttu-id="4dad2-120">802.11 i dispositivi possono usare OFDM.</span><span class="sxs-lookup"><span data-stu-id="4dad2-120">802.11a devices can use OFDM.</span></span>

</dd> <dt>

<span data-ttu-id="4dad2-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11 \_ di \_ Tipo PHY \_ hrdsss**</span><span class="sxs-lookup"><span data-stu-id="4dad2-121"><span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11\_phy\_type\_hrdsss**</span></span>
</dt> <dd>

<span data-ttu-id="4dad2-122">Specifica un tipo PHY DSSS (HRDSSS) ad alta frequenza.</span><span class="sxs-lookup"><span data-stu-id="4dad2-122">Specifies a high-rate DSSS (HRDSSS) PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="4dad2-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**\_ERP di \_ tipo \_ PHY dot11**</span><span class="sxs-lookup"><span data-stu-id="4dad2-123"><span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**dot11\_phy\_type\_erp**</span></span>
</dt> <dd>

<span data-ttu-id="4dad2-124">Specifica un tipo di PHY con frequenza estesa (ERP).</span><span class="sxs-lookup"><span data-stu-id="4dad2-124">Specifies an extended rate PHY type (ERP).</span></span> <span data-ttu-id="4dad2-125">i dispositivi 802.11 g possono usare ERP.</span><span class="sxs-lookup"><span data-stu-id="4dad2-125">802.11g devices can use ERP.</span></span>

</dd> <dt>

<span data-ttu-id="4dad2-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11 \_ PHY di \_ tipo \_ HT**</span><span class="sxs-lookup"><span data-stu-id="4dad2-126"><span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11\_phy\_type\_ht**</span></span>
</dt> <dd>

<span data-ttu-id="4dad2-127">Specifica il tipo PHY 802.11 n.</span><span class="sxs-lookup"><span data-stu-id="4dad2-127">Specifies the 802.11n PHY type.</span></span>

</dd> <dt>

<span data-ttu-id="4dad2-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**dot11 \_ di \_ Tipo PHY \_ VHT**</span><span class="sxs-lookup"><span data-stu-id="4dad2-128"><span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**dot11\_phy\_type\_vht**</span></span>
</dt> <dd>

<span data-ttu-id="4dad2-129">Specifica il tipo PHY AC 802.11.</span><span class="sxs-lookup"><span data-stu-id="4dad2-129">Specifies the 802.11ac PHY type.</span></span> <span data-ttu-id="4dad2-130">Si tratta del tipo PHY con velocità effettiva molto elevata specificato in IEEE 802.11 AC.</span><span class="sxs-lookup"><span data-stu-id="4dad2-130">This is the very high throughput PHY type specified in IEEE 802.11ac.</span></span>

<span data-ttu-id="4dad2-131">Questo valore è supportato in Windows 8.1, Windows Server 2012 R2 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4dad2-131">This value is supported on Windows 8.1, Windows Server 2012 R2, and later.</span></span>

</dd> <dt>

<span data-ttu-id="4dad2-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**\_ \_ avvio IHV dot11 tipo PHY \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4dad2-132"><span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**dot11\_phy\_type\_IHV\_start**</span></span>
</dt> <dd>

<span data-ttu-id="4dad2-133">Specifica l'inizio dell'intervallo utilizzato per definire i tipi PHY sviluppati da un fornitore di hardware indipendente (IHV).</span><span class="sxs-lookup"><span data-stu-id="4dad2-133">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="4dad2-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**dot11 \_ PHY \_ digitare \_ IHV \_ end**</span><span class="sxs-lookup"><span data-stu-id="4dad2-134"><span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**dot11\_phy\_type\_IHV\_end**</span></span>
</dt> <dd>

<span data-ttu-id="4dad2-135">Specifica l'inizio dell'intervallo utilizzato per definire i tipi PHY sviluppati da un fornitore di hardware indipendente (IHV).</span><span class="sxs-lookup"><span data-stu-id="4dad2-135">Specifies the start of the range that is used to define PHY types that are developed by an independent hardware vendor (IHV).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4dad2-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="4dad2-136">Remarks</span></span>

<span data-ttu-id="4dad2-137">Un IHV può assegnare un valore per i tipi PHY proprietari da **dot11 \_ PHY \_ Type \_ IHV \_ Start** through **dot11 \_ PHY \_ Type \_ IHV \_ end**.</span><span class="sxs-lookup"><span data-stu-id="4dad2-137">An IHV can assign a value for its proprietary PHY types from **dot11\_phy\_type\_IHV\_start** through **dot11\_phy\_type\_IHV\_end**.</span></span> <span data-ttu-id="4dad2-138">IHV deve assegnare un numero univoco da questo intervallo per ogni tipo di PHY proprietario.</span><span class="sxs-lookup"><span data-stu-id="4dad2-138">The IHV must assign a unique number from this range for each of its proprietary PHY types.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dad2-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4dad2-139">Requirements</span></span>



| <span data-ttu-id="4dad2-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dad2-140">Requirement</span></span> | <span data-ttu-id="4dad2-141">Valore</span><span class="sxs-lookup"><span data-stu-id="4dad2-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4dad2-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dad2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="4dad2-143">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="4dad2-143">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="4dad2-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dad2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="4dad2-145">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4dad2-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4dad2-146">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="4dad2-146">Redistributable</span></span><br/>          | <span data-ttu-id="4dad2-147">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="4dad2-147">Wireless LAN API for Windows XP with SP2</span></span><br/>                                   |
| <span data-ttu-id="4dad2-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4dad2-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dad2-149"><dt>Windot11. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dad2-149"><dt>Windot11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dad2-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4dad2-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dad2-151">**\_attributi di associazione WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="4dad2-151">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="4dad2-152">**\_funzionalità dell'interfaccia WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="4dad2-152">**WLAN\_INTERFACE\_CAPABILITY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




