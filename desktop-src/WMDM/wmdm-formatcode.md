---
title: Enumerazione WMDM_FORMATCODE
description: Il \_ tipo di enumerazione WMDM FORMATCODE definisce un elenco di codici di formato che descrivono i tipi di contenuto trasferiti da e verso un dispositivo.
ms.assetid: 203d9bdf-cbbd-4d06-8292-26c8a472e2aa
keywords:
- Enumerazione WMDM_FORMATCODE Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_FORMATCODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04db31578f36455fdf77bb4044ad45e5ca9f9a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324226"
---
# <a name="wmdm_formatcode-enumeration"></a>\_Enumerazione WMDM FORMATCODE

Il tipo di enumerazione **WMDM \_ FORMATCODE** definisce un elenco di codici di formato che descrivono i tipi di contenuto trasferiti da e verso un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWMDM_FORMATCODE { 
  WMDM_FORMATCODE_NOTUSED,
  WMDM_FORMATCODE_ALLIMAGES,
  WMDM_FORMATCODE_UNDEFINED,
  WMDM_FORMATCODE_ASSOCIATION,
  WMDM_FORMATCODE_SCRIPT,
  WMDM_FORMATCODE_EXECUTABLE,
  WMDM_FORMATCODE_TEXT,
  WMDM_FORMATCODE_HTML,
  WMDM_FORMATCODE_DPOF,
  WMDM_FORMATCODE_AIFF,
  WMDM_FORMATCODE_WAVE,
  WMDM_FORMATCODE_MP3,
  WMDM_FORMATCODE_AVI,
  WMDM_FORMATCODE_MPEG,
  WMDM_FORMATCODE_ASF,
  WMDM_FORMATCODE_RESERVED_FIRST,
  WMDM_FORMATCODE_RESERVED_LAST,
  WMDM_FORMATCODE_IMAGE_UNDEFINED,
  WMDM_FORMATCODE_IMAGE_EXIF,
  WMDM_FORMATCODE_IMAGE_TIFFEP,
  WMDM_FORMATCODE_IMAGE_FLASHPIX,
  WMDM_FORMATCODE_IMAGE_BMP,
  WMDM_FORMATCODE_IMAGE_CIFF,
  WMDM_FORMATCODE_IMAGE_GIF,
  WMDM_FORMATCODE_IMAGE_JFIF,
  WMDM_FORMATCODE_IMAGE_PCD,
  WMDM_FORMATCODE_IMAGE_PICT,
  WMDM_FORMATCODE_IMAGE_PNG,
  WMDM_FORMATCODE_IMAGE_TIFF,
  WMDM_FORMATCODE_IMAGE_TIFFIT,
  WMDM_FORMATCODE_IMAGE_JP2,
  WMDM_FORMATCODE_IMAGE_JPX,
  WMDM_FORMATCODE_IMAGE_RESERVED_FIRST,
  WMDM_FORMATCODE_IMAGE_RESERVED_LAST,
  WMDM_FORMATCODE_UNDEFINEDFIRMWARE,
          WMDM_FORMATCODE_WBMP
,
                  WMDM_FORMATCODE_JPEGXR
,
  WMDM_FORMATCODE_WINDOWSIMAGEFORMAT,
  WMDM_FORMATCODE_UNDEFINEDAUDIO,
  WMDM_FORMATCODE_WMA,
  WMDM_FORMATCODE_OGG,
  WMDM_FORMATCODE_AAC,
  WMDM_FORMATCODE_AUDIBLE,
  WMDM_FORMATCODE_FLAC,
          WMDM_FORMATCODE_QCELP
,
          WMDM_FORMATCODE_AMR
,
  WMDM_FORMATCODE_UNDEFINEDVIDEO,
  WMDM_FORMATCODE_WMV,
  WMDM_FORMATCODE_MP4,
  WMDM_FORMATCODE_MP2,
          WMDM_FORMATCODE_3G2
,
                  WMDM_FORMATCODE_AVCHD
,
                  WMDM_FORMATCODE_ATSCTS
,
                          WMDM_FORMATCODE_DVBTS
,
  WMDM_FORMATCODE_UNDEFINEDCOLLECTION,
  WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM,
  WMDM_FORMATCODE_ABSTRACTIMAGEALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOALBUM,
  WMDM_FORMATCODE_ABSTRACTVIDEOALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST,
  WMDM_FORMATCODE_ABSTRACTCONTACTGROUP,
  WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER,
  WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION,
  WMDM_FORMATCODE_WPLPLAYLIST,
  WMDM_FORMATCODE_M3UPLAYLIST,
  WMDM_FORMATCODE_MPLPLAYLIST,
  WMDM_FORMATCODE_ASXPLAYLIST,
  WMDM_FORMATCODE_PLSPLAYLIST,
  WMDM_FORMATCODE_UNDEFINEDDOCUMENT,
  WMDM_FORMATCODE_ABSTRACTDOCUMENT,
  WMDM_FORMATCODE_XMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT,
  WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET,
  WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT,
  WMDM_FORMATCODE_UNDEFINEDMESSAGE,
  WMDM_FORMATCODE_ABSTRACTMESSAGE,
  WMDM_FORMATCODE_UNDEFINEDCONTACT,
  WMDM_FORMATCODE_ABSTRACTCONTACT,
  WMDM_FORMATCODE_VCARD2,
  WMDM_FORMATCODE_VCARD3,
  WMDM_FORMATCODE_UNDEFINEDCALENDARITEM,
  WMDM_FORMATCODE_ABSTRACTCALENDARITEM,
  WMDM_FORMATCODE_VCALENDAR1,
  WMDM_FORMATCODE_VCALENDAR2,
  WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE,
  WMDM_FORMATCODE_MEDIA_CAST,
  WMDM_FORMATCODE_SECTION,
                                  WMDM_FORMATCODE_3G2A

} WMDM_FORMATCODE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM \_ FORMATCODE \_ abituata**
</dt> <dd>

Non viene utilizzato alcun codice di formato.

</dd> <dt>

<span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM \_ FORMATCODE \_ ALLIMAGES**
</dt> <dd>

Codice di formattazione che può essere utilizzato per eseguire una query per tutte le immagini.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**FORMATCODE WMDM non \_ \_ definito**
</dt> <dd>

Codice del formato utilizzato per eseguire una query per tutti gli oggetti non definiti.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**\_associazione WMDM FORMATCODE \_**
</dt> <dd>

Codice del formato utilizzato per definire un collegamento tra due oggetti.

</dd> <dt>

<span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**\_script WMDM FORMATCODE \_**
</dt> <dd>

Formattare il codice per un file di script.

</dd> <dt>

<span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**\_ \_ eseguibile WMDM FORMATCODE**
</dt> <dd>

Formattare il codice per un file eseguibile.

</dd> <dt>

<span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**\_testo FORMATCODE \_ WMDM**
</dt> <dd>

Formattare il codice per un file di testo.

</dd> <dt>

<span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM \_ FORMATCODE \_ HTML**
</dt> <dd>

Formattare il codice per un file HTML.

</dd> <dt>

<span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM \_ FORMATCODE \_ DPOF**
</dt> <dd>

Codice del formato utilizzato per rappresentare il formato dell'ordine di stampa digitale.

</dd> <dt>

<span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM \_ FORMATCODE \_ AIFF**
</dt> <dd>

Codice del formato utilizzato per rappresentare il formato del file di interscambio audio.

</dd> <dt>

<span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM \_ FORMATCODE \_ Wave**
</dt> <dd>

Codice di formattazione usato per un file WAV.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM \_ FORMATCODE \_ MP3**
</dt> <dd>

Codice di formattazione usato per un file MP3.

</dd> <dt>

<span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM \_ FORMATCODE \_ AVI**
</dt> <dd>

Codice di formattazione usato per un file AVI.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM \_ FORMATCODE \_ MPEG**
</dt> <dd>

Codice di formattazione usato per un file MPEG.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM \_ FORMATCODE \_ ASF**
</dt> <dd>

Codice del formato utilizzato per rappresentare un file di formato di sistema avanzato (ASF).

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM \_ FORMATCODE \_ riservato per \_ primo**
</dt> <dd>

Formattare il codice che è il primo in un intervallo riservato a PTP (Picture Transfer Protocol).

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM \_ FORMATCODE \_ riservato per \_ ultimo**
</dt> <dd>

Formattare il codice che è l'ultimo in un intervallo riservato per PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**\_immagine FORMATCODE WMDM non \_ \_ definita**
</dt> <dd>

Codice del formato utilizzato per rappresentare l'immagine di un tipo non definito.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM \_ FORMATCODE \_ Image \_ EXIF**
</dt> <dd>

Formattare il codice per un file EXIF. Usato anche per le immagini JPEG non coperte da WMDM \_ FORMATCODE \_ Image \_ JP2 o WMDM \_ FORMATCODE \_ Image \_ JPX.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM \_ FORMATCODE \_ Image \_ TIFFEP**
</dt> <dd>

Codice di formattazione usato per le immagini di tipo Tagged Image File Format per la fotografia elettronica (TIFF/EP)

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM \_ FORMATCODE \_ Image \_ FlashPix**
</dt> <dd>

Formattare il codice per un file di tipo FPX.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM \_ \_ immagine \_ BMP FORMATCODE**
</dt> <dd>

Formattare il codice per un file di tipo BMP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM \_ FORMATCODE \_ Image \_ CIFF**
</dt> <dd>

Formattare il codice per un'immagine nel formato di file dell'immagine della fotocamera.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**\_ \_ gif immagine FORMATCODE \_ WMDM**
</dt> <dd>

Formattare il codice per un file GIF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM \_ FORMATCODE \_ Image \_ JFIF**
</dt> <dd>

Formattare il codice per un file di tipo JFIF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM \_ FORMATCODE \_ Image \_ PCD**
</dt> <dd>

Formattare il codice per un'immagine di tipo CD foto.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM \_ FORMATCODE \_ Image \_ PICT**
</dt> <dd>

Formattare il codice per un'immagine di tipo PICT.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**\_ \_ png immagine WMDM \_ FORMATCODE**
</dt> <dd>

Formattare il codice per un'immagine di tipo PNG.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**\_ \_ TIFF immagine FORMATCODE \_ WMDM**
</dt> <dd>

Formattare il codice per un file di tipo TIFF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM \_ FORMATCODE \_ Image \_ TIFFIT**
</dt> <dd>

Formattare il codice per un'immagine di tipo Tagged Image File Format con la tecnologia di immagine.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM \_ FORMATCODE \_ Image \_ JP2**
</dt> <dd>

Formattare il codice per un'immagine JPEG200.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**WMDM \_ FORMATCODE \_ Image \_ JPX**
</dt> <dd>

Formattare il codice per un'immagine basata su JPEG200, usando la registrazione di immagini ancora estese. L'estensione del nome file è in genere. JPF o. JPX.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**WMDM \_ FORMATCODE \_ Image \_ riservato per \_ primo**
</dt> <dd>

Formattare il codice che è il primo in un intervallo riservato per un riferimento a un'immagine in PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**WMDM \_ FORMATCODE \_ Image \_ reserved \_ Last**
</dt> <dd>

Formattare il codice che rappresenta l'ultimo in un intervallo riservato per un riferimento a un'immagine in PTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDFIRMWARE**
</dt> <dd>

Formattare il codice quando il firmware non è definito.

</dd> <dt>

<span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**WMDM \_ \_WBMP FORMATCODE** 
</dt> <dd>

Formattare il codice per un'immagine di bitmap Wireless Application Protocol (wbmp).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**WMDM \_ \_JPEGXR FORMATCODE** 
</dt> <dd>

Formattare il codice per un'immagine della foto HD

</dd> <dt>

<span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT**
</dt> <dd>

Formattare il codice per il formato di immagine Windows.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO**
</dt> <dd>

Formattare il codice per un file audio di tipo non definito.

</dd> <dt>

<span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM \_ FORMATCODE \_ WMA**
</dt> <dd>

Formattare il codice per un file di Windows Media Audio (WMA).

</dd> <dt>

<span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM \_ FORMATCODE \_ OGG**
</dt> <dd>

Formattare il codice per un file audio con codifica Vorbis in un contenitore Ogg.

</dd> <dt>

<span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM \_ FORMATCODE \_ AAC**
</dt> <dd>

Formattare il codice per un file AAC (Advanced Audio Coding).

</dd> <dt>

<span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM \_ FORMATCODE \_ udibile**
</dt> <dd>

Formattare il codice per un file acustico.

</dd> <dt>

<span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM \_ FORMATCODE \_ FLAC**
</dt> <dd>

Formattare il codice per un file FLAC (lossless audio codec) gratuito.

</dd> <dt>

<span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**WMDM \_ \_QCELP FORMATCODE** 
</dt> <dd>

Codice di formattazione per un file di codec QCELP (codice Qualcomm Excited Linear Prediction).

</dd> <dt>

<span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**WMDM \_ \_AMR FORMATCODE** 
</dt> <dd>

Formattare il codice per un file di codec AMR (Adaptive multirate audio).

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO**
</dt> <dd>

Formattare il codice per un file video con un tipo non definito.

</dd> <dt>

<span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM \_ FORMATCODE \_ WMV**
</dt> <dd>

Formattare il codice per un file di Windows Media Video (WMV).

</dd> <dt>

<span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM \_ FORMATCODE \_ MP4**
</dt> <dd>

Formattare il codice per un file MP4.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM \_ FORMATCODE \_ MP2**
</dt> <dd>

Formattare il codice per un file MP2.

</dd> <dt>

<span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**WMDM \_ FORMATCODE \_ 3G2** 
</dt> <dd>

Formattare il codice per un formato del contenitore multimediale 3G2 (3GPP2). Un file di questo tipo può contenere audio, video o testo.

</dd> <dt>

<span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**WMDM \_ FORMATCODE \_ AVCHD** 
</dt> <dd>

Formattare il codice per un file video AVCHD (Advanced Video Coding High Definition).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**WMDM \_ FORMATCODE \_** 
</dt> <dd>

Formattare il codice per lo standard del formato ATSCs (Advanced Television Systems Committee).

</dd> <dt>

<span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**WMDM \_ \_DVBTS FORMATCODE** 
</dt> <dd>

Formattare il codice per un video MPEG-2 e MPEG-1 Layer II, oppure AC-3, audio all'interno di un flusso di trasporto MPEG-2 conforme a DVB.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM \_ FORMATCODE \_ undefined**
</dt> <dd>

Formattare il codice per una raccolta di un tipo non definito.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMULTIMEDIAALBUM**
</dt> <dd>

Formattare il codice per un album multimediale in cui l'oggetto contiene le proprietà di un album multimediale e, facoltativamente, i dati. Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTIMAGEALBUM**
</dt> <dd>

Formattare il codice per un album di immagini in cui l'oggetto contiene le proprietà di un album di immagini e, facoltativamente, i dati. Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTAUDIOALBUM**
</dt> <dd>

Formattare il codice per un album audio in cui l'oggetto contiene le proprietà di un album audio e, facoltativamente, i dati. Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTVIDEOALBUM**
</dt> <dd>

Formattare il codice per un album video in cui l'oggetto contiene le proprietà di un album video e, facoltativamente, i dati. Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST**
</dt> <dd>

Formattare il codice per una playlist audio/video in cui l'oggetto contiene le proprietà di una playlist audio/video e, facoltativamente, i dati. Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACTGROUP**
</dt> <dd>

Formattare il codice per un gruppo di contatti in cui l'oggetto contiene le proprietà di un gruppo di contatti e, facoltativamente, i dati. Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGEFOLDER**
</dt> <dd>

Formattare il codice per una cartella di messaggi in cui l'oggetto contiene le proprietà di una cartella del messaggio e, facoltativamente, i dati. Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCHAPTEREDPRODUCTION**
</dt> <dd>

Formattare il codice per una produzione con capitolo in cui l'oggetto contiene le proprietà di una produzione con capitoli e, facoltativamente, i dati. Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM \_ FORMATCODE \_ WPLPLAYLIST**
</dt> <dd>

Formattare il codice per una playlist formattata con la formattazione Windows Media playlist.

</dd> <dt>

<span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM \_ FORMATCODE \_ M3UPLAYLIST**
</dt> <dd>

Formattare il codice per una playlist con la formattazione M3U.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM \_ FORMATCODE \_ MPLPLAYLIST**
</dt> <dd>

Formattare il codice per una playlist con formattazione MPL.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM \_ FORMATCODE \_ ASXPLAYLIST**
</dt> <dd>

Formattare il codice per una playlist con formattazione ASX.

</dd> <dt>

<span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM \_ FORMATCODE \_ PLSPLAYLIST**
</dt> <dd>

Formattare il codice per una playlist con la formattazione dei PLS.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDDOCUMENT**
</dt> <dd>

Formattare il codice per un documento di tipo non definito.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM \_ FORMATCODE \_ ABSTRACTDOCUMENT**
</dt> <dd>

Formattare il codice per un documento in cui l'oggetto contiene le proprietà di un documento e, facoltativamente, i dati. Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**\_XMLDOCUMENT WMDM FORMATCODE \_**
</dt> <dd>

Formattare il codice per un documento XML.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM \_ FORMATCODE \_ MICROSOFTWORDDOCUMENT**
</dt> <dd>

Formattare il codice per un documento di Microsoft Word.

</dd> <dt>

<span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM \_ FORMATCODE \_ MHTCOMPILEDHTMLDOCUMENT**
</dt> <dd>

Formattare il codice per un documento HTML compilato.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM \_ FORMATCODE \_ MICROSOFTEXCELSPREADSHEET**
</dt> <dd>

Formattare il codice per un foglio di calcolo di Microsoft Excel.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM \_ FORMATCODE \_ MICROSOFTPOWERPOINTDOCUMENT**
</dt> <dd>

Formattare il codice per un documento di Microsoft PowerPoint.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDMESSAGE**
</dt> <dd>

Formattare il codice per un messaggio di tipo non definito.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGE**
</dt> <dd>

Formattare il codice per un messaggio in cui l'oggetto contiene le proprietà di un messaggio e, facoltativamente, i dati. Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCONTACT**
</dt> <dd>

Formattare il codice per un contatto di tipo non definito.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACT**
</dt> <dd>

Formattare il codice per un contatto in cui l'oggetto contiene le proprietà di un contatto e, facoltativamente, i dati. Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM \_ FORMATCODE \_ VCARD2**
</dt> <dd>

Formattare il codice per una scheda elettronica con la formattazione di vCard versione 2.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM \_ FORMATCODE \_ VCARD3**
</dt> <dd>

Formattare il codice per una scheda elettronica con la formattazione di vCard versione 3.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCALENDARITEM**
</dt> <dd>

Formattare il codice per un elemento del calendario elettronico di tipo non definito.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCALENDARITEM**
</dt> <dd>

Formattare il codice per un elemento del calendario in cui l'oggetto contiene le proprietà di un elemento del calendario e, facoltativamente, i dati. Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM \_ FORMATCODE \_ VCALENDAR1**
</dt> <dd>

Formattare il codice per un elemento del calendario elettronico con la formattazione della versione 1 di vCalendar.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM \_ FORMATCODE \_ VCALENDAR2**
</dt> <dd>

Formattare il codice per un elemento del calendario elettronico con la formattazione vCalendar versione 2.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDWINDOWSEXECUTABLE**
</dt> <dd>

Formattare il codice per un eseguibile basato su Windows di tipo non definito.

</dd> <dt>

<span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**\_ \_ cast multimediale WMDM \_ FORMATCODE**
</dt> <dd>

Formattare il codice per un oggetto cast multimediale.

</dd> <dt>

<span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**\_sezione WMDM FORMATCODE \_**
</dt> <dd>

Formattare il codice per una sezione di dati contenuta in un altro oggetto.

</dd> <dt>

<span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**WMDM \_ \_3G2A FORMATCODE** 
</dt> <dd>

Formattare il codice per un formato di contenitore multimediale 3G2A (3GPP2A).

</dd> </dl>

## <a name="remarks"></a>Commenti

Per individuare i formati supportati da un dispositivo, un'applicazione può usare [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) per eseguire query sulla proprietà del dispositivo **g \_ wszWMDMFormatsSupported** .

Per individuare le funzionalità del dispositivo per un particolare formato, un'applicazione può chiamare [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).

Un'applicazione può impostare il codice di formato durante la creazione di una risorsa di archiviazione nel dispositivo includendo la proprietà **g \_ wszWMDMFormatCode** nei metadati passati nel parametro *pMetaData* di una chiamata a [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).

Un'applicazione può eseguire una query sul codice del formato di un'archiviazione chiamando [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) e recuperando la proprietà **g \_ wszWMDMFormatCode** .

Se il dispositivo supporta l'impostazione del codice del formato dopo la creazione dello spazio di archiviazione, un'applicazione può usare [**IWMDMStorage3::**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) SetProperty per impostare la proprietà **g \_ wszWMDMFormatCode** . Alcuni dispositivi potrebbero non consentire la modifica del codice del formato dopo la creazione dell'archiviazione nel dispositivo. Pertanto, è consigliabile impostare questa proprietà insieme ai metadati passati in [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[**IWMDMStorage3:: tometadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[**Costanti dei metadati**](metadata-constants.md)
</dt> </dl>

 

 





