---
title: WMT_RIGHTS enumerazione (Wmdrmsdk.h)
description: Definisce i diritti che possono essere specificati in una licenza DRM.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- WMT_RIGHTS di enumerazione windows Media Format
- enumerazione windows Media Format
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
ms.openlocfilehash: 3a48c9ce3a276f060ac90dd15100ca8612e35116e124588e27f4ee36c1a0b8a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930741"
---
# <a name="wmt_rights-enumeration"></a>Enumerazione RIGHTS \_ WMT

Il **tipo di enumerazione \_ WMT RIGHTS** definisce i diritti che possono essere specificati in una licenza DRM.

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

<span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**RIPRODUZIONE A DESTRA WMT \_ \_**
</dt> <dd>

Specifica il diritto di riprodurre contenuto senza restrizioni.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**COPIA \_ DESTRA \_ WMT \_ IN UN DISPOSITIVO \_ NON \_ \_ SDMI**
</dt> <dd>

Specifica il diritto di copiare il contenuto in un dispositivo non conforme a Secure Digital Musica Initiative (SDMI).

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**COPIA \_ DESTRA \_ WMT \_ SU \_ CD**
</dt> <dd>

Specifica il diritto di copiare il contenuto in un CD.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**COPIA DESTRA WMT \_ \_ NEL DISPOSITIVO \_ \_ \_ SDMI**
</dt> <dd>

Specifica il diritto di copiare il contenuto in un dispositivo conforme a SDMI.

</dd> <dt>

<span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ DESTRA \_ UNA \_ VOLTA**
</dt> <dd>

Specifica il diritto di riprodurre il contenuto una sola volta.

</dd> <dt>

<span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT \_ RIGHT \_ SAVE \_ STREAM \_ PROTECTED**
</dt> <dd>

Specifica il diritto di salvare il contenuto da un server.

</dd> <dt>

<span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**COPIA DESTRA \_ WMT \_**
</dt> <dd>

Specifica il diritto di copiare il contenuto. Windows Media DRM 10 regola i dispositivi in cui è possibile copiare il contenuto usando i livelli di protezione dell'output (OPL).

</dd> <dt>

<span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**GIOCO COLLABORATIVO DI WMT \_ \_ \_ RIGHT**
</dt> <dd>

Specifica il diritto di riprodurre contenuto come parte di uno scenario online in cui più partecipanti possono contribuire a una playlist condivisa con i brani della raccolta.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**TRIGGER \_ \_ SDMI DESTRO WMT \_**
</dt> <dd>

Riservato per utilizzi futuri. Non usare.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**\_ \_ NOMORECOPIES SDMI \_ DESTRA WMT**
</dt> <dd>

Riservato per utilizzi futuri. Non usare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questi valori sono flag di bit, quindi è possibile impostare uno o più valori combinandoli con l'operatore **OR** bit per bit.

Quando si usa Windows Media DRM 10, **WMT \_ RIGHT COPY TO NON \_ \_ \_ \_ SDMI \_ DEVICE**, **WMT RIGHT COPY TO \_ \_ \_ \_ SDMI \_ DEVICE** e **WMT RIGHT COPY TO \_ \_ \_ \_ CD** vengono sostituite da **WMT RIGHT \_ \_ COPY**. Le limitazioni nei dispositivi in cui è possibile copiare il contenuto vengono specificate usando i livelli di protezione dell'output (OPL).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> </dl>

 

 





