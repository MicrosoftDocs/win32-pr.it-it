---
title: Enumerazione WMT_RIGHTS (wmdrmsdk. h)
description: Definisce i diritti che possono essere specificati in una licenza DRM.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- Formato Windows Media enumerazione WMT_RIGHTS
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- WMT_RIGHTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644cff9c94876fab11bc9fbe181ac0375d9444fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324048"
---
# <a name="wmt_rights-enumeration"></a>\_Enumerazione dei diritti WMT

Il tipo di enumerazione **\_ dei diritti WMT** definisce i diritti che possono essere specificati in una licenza DRM.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WMT_RIGHTS { 
  WMT_RIGHT_PLAYBACK                 = 0x00000001,
  WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE  = 0x00000002,
  WMT_RIGHT_COPY_TO_CD               = 0x00000008,
  WMT_RIGHT_COPY_TO_SDMI_DEVICE      = 0x00000010,
  WMT_RIGHT_ONE_TIME                 = 0x00000020,
  WMT_RIGHT_SAVE_STREAM_PROTECTED    = 0x00000040,
  WMT_RIGHT_COPY                     = 0x00000080,
  WMT_RIGHT_COLLABORATIVE_PLAY       = 0x00000100,
  WMT_RIGHT_SDMI_TRIGGER             = 0x00010000,
  WMT_RIGHT_SDMI_NOMORECOPIES        = 0x00020000
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT \_ riproduzione a destra \_**
</dt> <dd>

Specifica il diritto di riprodurre il contenuto senza restrizioni.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**WMT \_ \_ Copia \_ a destra \_ nel \_ dispositivo non SDMI \_**
</dt> <dd>

Specifica il diritto di copiare il contenuto in un dispositivo non conforme a Secure Digital Music Initiative (SDMI).

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT \_ \_ Copia \_ a destra su \_ CD**
</dt> <dd>

Specifica il diritto di copiare il contenuto in un CD.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT \_ \_ Copia \_ a destra \_ nel \_ dispositivo SDMI**
</dt> <dd>

Specifica il diritto di copiare il contenuto in un dispositivo conforme a SDMI.

</dd> <dt>

<span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ giusto \_ una \_ volta**
</dt> <dd>

Specifica il diritto di riprodurre il contenuto solo una volta.

</dd> <dt>

<span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT \_ right \_ Salva \_ flusso \_ protetto**
</dt> <dd>

Specifica il diritto di salvare il contenuto da un server.

</dd> <dt>

<span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT \_ copia a destra \_**
</dt> <dd>

Specifica il diritto di copiare il contenuto. Windows Media DRM 10 regola i dispositivi ai quali è possibile copiare il contenuto usando i livelli di protezione dell'output (OPLs).

</dd> <dt>

<span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT \_ right \_ collaborative \_ Play**
</dt> <dd>

Specifica il diritto di riprodurre il contenuto come parte di uno scenario online in cui più partecipanti possono contribuire con i brani della raccolta a una playlist condivisa.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**\_trigger WMT Right \_ SDMI \_**
</dt> <dd>

Riservato per utilizzi futuri. Non usare.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT \_ right \_ SDMI \_ NOMORECOPIES**
</dt> <dd>

Riservato per utilizzi futuri. Non usare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questi valori sono flag di bit, quindi uno o più possono essere impostati combinando questi valori con **l'operatore OR** bit per bit.

Quando si usa Windows Media DRM 10 **, WMT \_ right \_ copy \_ to \_ non \_ SDMI \_ Device**, **WMT \_ right \_ copy \_ to \_ SDMI \_ Device** e **WMT \_ right \_ copy \_ to \_ CD** sono sostituiti da **WMT \_ right \_ Copy**. Le limitazioni nei dispositivi in cui è possibile copiare il contenuto vengono specificate usando i livelli di protezione dell'output (OPLs).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> </dl>

 

 





