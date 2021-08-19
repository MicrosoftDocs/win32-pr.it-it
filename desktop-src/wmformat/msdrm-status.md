---
title: MSDRM_STATUS enumerazione (Wmdrmsdk.h)
description: Il tipo di enumerazione \_ MSDRM STATUS definisce le condizioni di stato per il sottosistema DRM.
ms.assetid: b26600ea-2603-4fca-9408-2d5c88091dcc
keywords:
- MSDRM_STATUS enumerazione Windows Media Format
- enumeration windows Media Format
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
ms.openlocfilehash: 0c4c1f9b37f237b1ae2399849ef3100e3d6fdbc12c7ee3bc1d169420e38bb85a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117654575"
---
# <a name="msdrm_status-enumeration"></a>Enumerazione MSDRM \_ STATUS

Il **tipo di enumerazione \_ MSDRM STATUS** definisce le condizioni di stato per il sottosistema DRM.

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

<span id="DRM_ERROR"></span><span id="drm_error"></span>**ERRORE \_ DRM**
</dt> <dd>

Specifica che si è verificato un errore.

</dd> <dt>

<span id="DRM_INFORMATION"></span><span id="drm_information"></span>**INFORMAZIONI \_ DRM**
</dt> <dd>

Specifica che sono disponibili informazioni aggiuntive sullo stato.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM \_ BACKUPRESTORE \_ BEGIN**
</dt> <dd>

Specifica che è stata avviata un'operazione di backup o ripristino delle licenze.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**FINE \_ BACKUPRESTORE DRM \_**
</dt> <dd>

Specifica che un'operazione di backup o ripristino della licenza è terminata.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**BACKUP \_ DRMRESTORE \_ CONNECTING**
</dt> <dd>

Specifica che è in corso un'operazione di backup o ripristino delle licenze e che il computer client si connette al server di backup.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**BACKUP DRM \_ DISCONNESSIONE \_ DEL RIPRISTINO**
</dt> <dd>

Specifica che è in corso un'operazione di backup o ripristino delle licenze e che il computer client si sta disconnettendo dal server di backup.

</dd> <dt>

<span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**ERRORE DRM \_ \_ WITHURL**
</dt> <dd>

Specifica che l'operazione DRM ha rilevato un URL non valido.

</dd> <dt>

<span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**LICENZA CON \_ RESTRIZIONI \_ DRM**
</dt> <dd>

Specifica che l'operazione DRM non può continuare perché nel computer client non esiste alcuna licenza che concede il diritto richiesto.

</dd> <dt>

<span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ RICHIEDE \_ L'INDIVIDUALIZZAZIONE**
</dt> <dd>

Specifica che l'operazione DRM non può continuare perché il sottosistema DRM deve essere individualizzato.

</dd> <dt>

<span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**NOTIFICA \_ \_ OPL DI RIPRODUZIONE \_ DRM**
</dt> <dd>

Specifica che non è possibile completare un'operazione di riproduzione perché non è stato soddisfatto un requisito del livello di protezione dell'output.

</dd> <dt>

<span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**NOTIFICA \_ \_ OPL COPIA \_ DRM**
</dt> <dd>

Specifica che non è possibile completare un'operazione di copia perché non è stato soddisfatto un requisito del livello di protezione dell'output.

</dd> <dt>

<span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**DRM \_ REFRESHCRL \_ COMPLETE**
</dt> <dd>

Specifica che una chiamata a [**IWMDRMSecurity::P erformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) ha completato l'aggiornamento di un elenco di revoche.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> </dl>

 

 





