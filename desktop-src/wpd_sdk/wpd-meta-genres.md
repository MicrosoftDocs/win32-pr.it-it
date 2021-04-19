---
description: Il \_ \_ tipo di enumerazione WPD meta genres descrive un tipo di genere generale di un file multimediale.
ms.assetid: a69cab70-5a45-4e75-abbd-230396c2b5ec
title: Enumerazione WPD_META_GENRES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_META_GENRES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f6ff4875474776df1e2436e0209e6d863f5b3e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325805"
---
# <a name="wpd_meta_genres-enumeration"></a>\_Enumerazione WPD meta \_ genres

Il tipo di enumerazione **WPD \_ meta \_ genres** descrive un tipo di genere generale di un file multimediale.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_META_GENRES { 
  WPD_META_GENRE_UNUSED                            = 0x0,
  WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE          = 0x1,
  WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE      = 0x11,
  WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES      = 0x12,
  WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK  = 0x13,
  WPD_META_GENRE_SPOKEN_WORD_NEWS                  = 0x14,
  WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS            = 0x15,
  WPD_META_GENRE_GENERIC_VIDEO_FILE                = 0x21,
  WPD_META_GENRE_NEWS_VIDEO_FILE                   = 0x22,
  WPD_META_GENRE_MUSIC_VIDEO_FILE                  = 0x23,
  WPD_META_GENRE_HOME_VIDEO_FILE                   = 0x24,
  WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE           = 0x25,
  WPD_META_GENRE_TELEVISION_VIDEO_FILE             = 0x26,
  WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE   = 0x27,
  WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE          = 0x28,
  WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO       = 0x30,
  WPD_META_GENRE_AUDIO_PODCAST                     = 0x40,
  WPD_META_GENRE_VIDEO_PODCAST                     = 0x41,
  WPD_META_GENRE_MIXED_PODCAST                     = 0x42
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**WPD \_ meta \_ genre non \_ usato**
</dt> <dd>

Il genere non è stato impostato o non è applicabile.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**\_ \_ \_ \_ file audio di musica generica WPD meta \_ genre \_**
</dt> <dd>

Si tratta di un file musicale generico (solo audio).

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**\_ \_ \_ \_ file audio generico non di \_ musica \_ WPD meta genre \_**
</dt> <dd>

Si tratta di un file audio non musicale generico, ad esempio un libro vocale o audio.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**\_file del \_ \_ \_ \_ libro audio della parola \_ del Metagenere WPD \_**
</dt> <dd>

Si tratta di un file di libro audio.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD \_ \_ \_ i file di Word pronunciati del Metagenere \_ \_ \_ non \_ audio \_ book**
</dt> <dd>

Si tratta di un file audio di parole pronunciate che non è un libro audio, ad esempio un'intervista o un discorso.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**\_notizie di \_ \_ parole parlate Metagenere WPD \_ \_**
</dt> <dd>

Si tratta di un file audio o video di notizie.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**Mostra la parola parlata \_ \_ METAgenere WPD \_ \_ \_ \_**
</dt> <dd>

Si tratta di una registrazione audio di una presentazione Talk.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**\_ \_ \_ \_ file video generico WPD meta \_ genre**
</dt> <dd>

Si tratta di un file video generico.

</dd> <dt>

<span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**\_ \_ \_ file video di News meta genre \_ WPD \_**
</dt> <dd>

Si tratta di un file video di notizie.

</dd> <dt>

<span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**\_file video WPD meta \_ genre \_ Music \_ \_**
</dt> <dd>

Si tratta di un file video musicale.

</dd> <dt>

<span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**\_ \_ \_ \_ file video Home WPD meta \_ genre**
</dt> <dd>

Si tratta di un file video Home.

</dd> <dt>

<span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**\_ \_ \_ \_ \_ file video della funzionalità WPD meta \_ genre**
</dt> <dd>

Si tratta di un file video con funzionalità di film.

</dd> <dt>

<span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**\_file video WPD meta \_ genre \_ Television \_ \_**
</dt> <dd>

Si tratta di un file video del programma TV.

</dd> <dt>

<span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**\_ \_ \_ \_ file video didattico WPD \_ meta genere Training \_**
</dt> <dd>

Si tratta di un file video didattico.

</dd> <dt>

<span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**\_file video di WPD meta \_ genre \_ Photo \_ Montage \_ \_**
</dt> <dd>

Si tratta di un file video con un fotomontaggio foto.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**WPD \_ \_ \_ non audio generico di meta genere non \_ \_ \_ \_ video**
</dt> <dd>

Si tratta di un file senza audio o video.

</dd> <dt>

<span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**\_ \_ \_ podcast audio WPD meta \_ genre**
</dt> <dd>

Si tratta di un podcast audio.

</dd> <dt>

<span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**PODCAST video di WPD \_ meta \_ genre \_ \_**
</dt> <dd>

Si tratta di un podcast video.

</dd> <dt>

<span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**\_ \_ \_ podcast misto WPD meta \_ genre**
</dt> <dd>

Si tratta di un podcast che contiene audio e video.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla proprietà [WPD \_ media \_ meta \_ genre](media-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




