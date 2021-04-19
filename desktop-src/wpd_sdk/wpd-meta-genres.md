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
# <a name="wpd_meta_genres-enumeration"></a><span data-ttu-id="a910b-103">\_Enumerazione WPD meta \_ genres</span><span class="sxs-lookup"><span data-stu-id="a910b-103">WPD\_META\_GENRES enumeration</span></span>

<span data-ttu-id="a910b-104">Il tipo di enumerazione **WPD \_ meta \_ genres** descrive un tipo di genere generale di un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="a910b-104">The **WPD\_META\_GENRES** enumeration type describes a broad genre type of a media file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a910b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a910b-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="a910b-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="a910b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a910b-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**WPD \_ meta \_ genre non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="a910b-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**WPD\_META\_GENRE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-108">Il genere non è stato impostato o non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="a910b-108">The genre has not been set, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**\_ \_ \_ \_ file audio di musica generica WPD meta \_ genre \_**</span><span class="sxs-lookup"><span data-stu-id="a910b-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-110">Si tratta di un file musicale generico (solo audio).</span><span class="sxs-lookup"><span data-stu-id="a910b-110">This is a generic music file (audio only).</span></span>

</dd> <dt>

<span data-ttu-id="a910b-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**\_ \_ \_ \_ file audio generico non di \_ musica \_ WPD meta genre \_**</span><span class="sxs-lookup"><span data-stu-id="a910b-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-112">Si tratta di un file audio non musicale generico, ad esempio un libro vocale o audio.</span><span class="sxs-lookup"><span data-stu-id="a910b-112">This is a generic non-music audio file, for example, a speech or audio book.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**\_file del \_ \_ \_ \_ libro audio della parola \_ del Metagenere WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a910b-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_AUDIO\_BOOK\_FILES**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-114">Si tratta di un file di libro audio.</span><span class="sxs-lookup"><span data-stu-id="a910b-114">This is an audio book file.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD \_ \_ \_ i file di Word pronunciati del Metagenere \_ \_ \_ non \_ audio \_ book**</span><span class="sxs-lookup"><span data-stu-id="a910b-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_FILES\_NON\_AUDIO\_BOOK**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-116">Si tratta di un file audio di parole pronunciate che non è un libro audio, ad esempio un'intervista o un discorso.</span><span class="sxs-lookup"><span data-stu-id="a910b-116">This is a spoken-word audio file that is not an audio book, for example, an interview or speech.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**\_notizie di \_ \_ parole parlate Metagenere WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a910b-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_NEWS**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-118">Si tratta di un file audio o video di notizie.</span><span class="sxs-lookup"><span data-stu-id="a910b-118">This is a news audio or video file.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**Mostra la parola parlata \_ \_ METAgenere WPD \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a910b-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_TALK\_SHOWS**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-120">Si tratta di una registrazione audio di una presentazione Talk.</span><span class="sxs-lookup"><span data-stu-id="a910b-120">This is an audio recording of a talk show.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**\_ \_ \_ \_ file video generico WPD meta \_ genre**</span><span class="sxs-lookup"><span data-stu-id="a910b-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**WPD\_META\_GENRE\_GENERIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-122">Si tratta di un file video generico.</span><span class="sxs-lookup"><span data-stu-id="a910b-122">This is a generic video file.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**\_ \_ \_ file video di News meta genre \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="a910b-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**WPD\_META\_GENRE\_NEWS\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-124">Si tratta di un file video di notizie.</span><span class="sxs-lookup"><span data-stu-id="a910b-124">This is a news video file.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**\_file video WPD meta \_ genre \_ Music \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a910b-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**WPD\_META\_GENRE\_MUSIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-126">Si tratta di un file video musicale.</span><span class="sxs-lookup"><span data-stu-id="a910b-126">This is a music video file.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**\_ \_ \_ \_ file video Home WPD meta \_ genre**</span><span class="sxs-lookup"><span data-stu-id="a910b-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**WPD\_META\_GENRE\_HOME\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-128">Si tratta di un file video Home.</span><span class="sxs-lookup"><span data-stu-id="a910b-128">This is a home video file.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**\_ \_ \_ \_ \_ file video della funzionalità WPD meta \_ genre**</span><span class="sxs-lookup"><span data-stu-id="a910b-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**WPD\_META\_GENRE\_FEATURE\_FILM\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-130">Si tratta di un file video con funzionalità di film.</span><span class="sxs-lookup"><span data-stu-id="a910b-130">This is a feature film video file.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**\_file video WPD meta \_ genre \_ Television \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a910b-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**WPD\_META\_GENRE\_TELEVISION\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-132">Si tratta di un file video del programma TV.</span><span class="sxs-lookup"><span data-stu-id="a910b-132">This is a television program video file.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**\_ \_ \_ \_ file video didattico WPD \_ meta genere Training \_**</span><span class="sxs-lookup"><span data-stu-id="a910b-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**WPD\_META\_GENRE\_TRAINING\_EDUCATIONAL\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-134">Si tratta di un file video didattico.</span><span class="sxs-lookup"><span data-stu-id="a910b-134">This is an educational video file.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**\_file video di WPD meta \_ genre \_ Photo \_ Montage \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a910b-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**WPD\_META\_GENRE\_PHOTO\_MONTAGE\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-136">Si tratta di un file video con un fotomontaggio foto.</span><span class="sxs-lookup"><span data-stu-id="a910b-136">This is a video file featuring a photo montage.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**WPD \_ \_ \_ non audio generico di meta genere non \_ \_ \_ \_ video**</span><span class="sxs-lookup"><span data-stu-id="a910b-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_AUDIO\_NON\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-138">Si tratta di un file senza audio o video.</span><span class="sxs-lookup"><span data-stu-id="a910b-138">This is a file without audio or video.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**\_ \_ \_ podcast audio WPD meta \_ genre**</span><span class="sxs-lookup"><span data-stu-id="a910b-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**WPD\_META\_GENRE\_AUDIO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-140">Si tratta di un podcast audio.</span><span class="sxs-lookup"><span data-stu-id="a910b-140">This is an audio podcast.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**PODCAST video di WPD \_ meta \_ genre \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a910b-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**WPD\_META\_GENRE\_VIDEO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-142">Si tratta di un podcast video.</span><span class="sxs-lookup"><span data-stu-id="a910b-142">This is a video podcast.</span></span>

</dd> <dt>

<span data-ttu-id="a910b-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**\_ \_ \_ podcast misto WPD meta \_ genre**</span><span class="sxs-lookup"><span data-stu-id="a910b-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**WPD\_META\_GENRE\_MIXED\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="a910b-144">Si tratta di un podcast che contiene audio e video.</span><span class="sxs-lookup"><span data-stu-id="a910b-144">This is a podcast containing both audio and video.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a910b-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="a910b-145">Remarks</span></span>

<span data-ttu-id="a910b-146">Questa enumerazione viene utilizzata dalla proprietà [WPD \_ media \_ meta \_ genre](media-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="a910b-146">This enumeration is used by the [WPD\_MEDIA\_META\_GENRE](media-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a910b-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a910b-147">Requirements</span></span>



| <span data-ttu-id="a910b-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="a910b-148">Requirement</span></span> | <span data-ttu-id="a910b-149">Valore</span><span class="sxs-lookup"><span data-stu-id="a910b-149">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a910b-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a910b-150">Header</span></span><br/> | <dl> <span data-ttu-id="a910b-151"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a910b-151"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a910b-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a910b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a910b-153">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="a910b-153">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




