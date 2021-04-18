---
title: Enumerazione MSDRM_STATUS (wmdrmsdk. h)
description: Il \_ tipo di enumerazione dello stato MSDRM definisce le condizioni di stato per il sottosistema DRM.
ms.assetid: b26600ea-2603-4fca-9408-2d5c88091dcc
keywords:
- Formato Windows Media enumerazione MSDRM_STATUS
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- MSDRM_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2a73de9e33216e22a01966be8f2ed6a3185fdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326960"
---
# <a name="msdrm_status-enumeration"></a>\_Enumerazione stato msdrm

Il tipo di enumerazione **\_ dello stato MSDRM** definisce le condizioni di stato per il sottosistema DRM.

## <a name="syntax"></a>Sintassi


```C++
typedef enum MSDRM_STATUS { 
  DRM_ERROR                        = 0,
  DRM_INFORMATION                  = 1,
  DRM_BACKUPRESTORE_BEGIN          = 2,
  DRM_BACKUPRESTORE_END            = 3,
  DRM_BACKUPRESTORE_CONNECTING     = 4,
  DRM_BACKUPRESTORE_DISCONNECTING  = 5,
  DRM_ERROR_WITHURL                = 6,
  DRM_RESTRICTED_LICENSE           = 7,
  DRM_NEEDS_INDIVIDUALIZATION      = 8,
  DRM_PLAY_OPL_NOTIFICATION        = 9,
  DRM_COPY_OPL_NOTIFICATION        = 10,
  DRM_REFRESHCRL_COMPLETE          = 11
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="DRM_ERROR"></span><span id="drm_error"></span>**\_errore DRM**
</dt> <dd>

Specifica che si è verificato un errore.

</dd> <dt>

<span id="DRM_INFORMATION"></span><span id="drm_information"></span>**\_informazioni DRM**
</dt> <dd>

Specifica che sono presenti informazioni aggiuntive sullo stato.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**\_inizio BACKUPRESTORE \_ DRM**
</dt> <dd>

Specifica l'inizio di un'operazione di backup o ripristino delle licenze.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**\_fine BACKUPRESTORE \_ DRM**
</dt> <dd>

Specifica che è stata terminata un'operazione di backup o ripristino delle licenze.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**\_connessione DRM BACKUPRESTORE \_**
</dt> <dd>

Specifica che è in corso un'operazione di backup o ripristino della licenza e che il computer client si connette al server di backup.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**disconnessione di \_ BACKUPRESTORE DRM \_**
</dt> <dd>

Specifica che è in corso un'operazione di backup o ripristino della licenza e che il computer client si sta disconnettendo dal server di backup.

</dd> <dt>

<span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**\_errore DRM \_ WITHURL**
</dt> <dd>

Specifica che l'operazione DRM ha rilevato un URL non valido.

</dd> <dt>

<span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**\_licenza con restrizioni DRM \_**
</dt> <dd>

Specifica che l'operazione di DRM non può continuare perché non è presente alcuna licenza che conceda il diritto richiesto nel computer client.

</dd> <dt>

<span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ necessita di un' \_ individualizzazione**
</dt> <dd>

Specifica che l'operazione DRM non può continuare perché il sottosistema DRM deve essere individualizzato.

</dd> <dt>

<span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**\_ \_ notifica OPL di riproduzione DRM \_**
</dt> <dd>

Specifica che non è possibile completare un'operazione di riproduzione perché non è stato soddisfatto un requisito del livello di protezione dell'output.

</dd> <dt>

<span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**\_ \_ notifica OPL copia \_ DRM**
</dt> <dd>

Specifica che non è possibile completare un'operazione di copia perché non è stato soddisfatto un requisito del livello di protezione dell'output.

</dd> <dt>

<span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**\_REFRESHCRL DRM \_ completato**
</dt> <dd>

Specifica che una chiamata a [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) ha completato l'aggiornamento di un elenco di revoche.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> </dl>

 

 





