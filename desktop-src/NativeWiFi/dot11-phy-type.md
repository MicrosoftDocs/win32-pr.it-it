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
# <a name="dot11_phy_type-enumeration"></a>\_Enumerazione del \_ Tipo PHY DOT11

L'enumerazione del **\_ \_ Tipo PHY DOT11** definisce un PHY 802,11 e un tipo di supporto.

## <a name="syntax"></a>Sintassi


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



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**\_Tipo PHY \_ dot11 \_ sconosciuto**
</dt> <dd>

Specifica un tipo PHY sconosciuto o non inizializzato.

</dd> <dt>

<span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**dot11 \_ PHY \_ digitare \_ any**
</dt> <dd>

Specifica qualsiasi tipo di PHY.

</dd> <dt>

<span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**dot11 \_ di \_ Tipo PHY \_ FHSS**
</dt> <dd>

Specifica un PHY FHSS (Frequency-Hopping Spread-Spectrum). I dispositivi Bluetooth possono usare FHSS o un adattamento di FHSS.

</dd> <dt>

<span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**dot11 \_ di \_ Tipo PHY \_ DSSS**
</dt> <dd>

Specifica un tipo di PHY DSSS (Direct Sequence Spread Spectrum).

</dd> <dt>

<span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**dot11 \_ di \_ Tipo PHY \_ irbaseband**
</dt> <dd>

Specifica un tipo PHY a infrarossi (IR).

</dd> <dt>

<span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**dot11 \_ di \_ Tipo PHY \_ OFDM**
</dt> <dd>

Specifica un tipo PHY OFDM (ortogonal Frequency Division Multiplexing). 802.11 i dispositivi possono usare OFDM.

</dd> <dt>

<span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**dot11 \_ di \_ Tipo PHY \_ hrdsss**
</dt> <dd>

Specifica un tipo PHY DSSS (HRDSSS) ad alta frequenza.

</dd> <dt>

<span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**\_ERP di \_ tipo \_ PHY dot11**
</dt> <dd>

Specifica un tipo di PHY con frequenza estesa (ERP). i dispositivi 802.11 g possono usare ERP.

</dd> <dt>

<span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**dot11 \_ PHY di \_ tipo \_ HT**
</dt> <dd>

Specifica il tipo PHY 802.11 n.

</dd> <dt>

<span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**dot11 \_ di \_ Tipo PHY \_ VHT**
</dt> <dd>

Specifica il tipo PHY AC 802.11. Si tratta del tipo PHY con velocità effettiva molto elevata specificato in IEEE 802.11 AC.

Questo valore è supportato in Windows 8.1, Windows Server 2012 R2 e versioni successive.

</dd> <dt>

<span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**\_ \_ avvio IHV dot11 tipo PHY \_ \_**
</dt> <dd>

Specifica l'inizio dell'intervallo utilizzato per definire i tipi PHY sviluppati da un fornitore di hardware indipendente (IHV).

</dd> <dt>

<span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**dot11 \_ PHY \_ digitare \_ IHV \_ end**
</dt> <dd>

Specifica l'inizio dell'intervallo utilizzato per definire i tipi PHY sviluppati da un fornitore di hardware indipendente (IHV).

</dd> </dl>

## <a name="remarks"></a>Commenti

Un IHV può assegnare un valore per i tipi PHY proprietari da **dot11 \_ PHY \_ Type \_ IHV \_ Start** through **dot11 \_ PHY \_ Type \_ IHV \_ end**. IHV deve assegnare un numero univoco da questo intervallo per ogni tipo di PHY proprietario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/>                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Windot11. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_attributi di associazione WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**\_funzionalità dell'interfaccia WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




