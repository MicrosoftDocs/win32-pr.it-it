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
# <a name="wmdm_formatcode-enumeration"></a><span data-ttu-id="9dd82-104">\_Enumerazione WMDM FORMATCODE</span><span class="sxs-lookup"><span data-stu-id="9dd82-104">WMDM\_FORMATCODE enumeration</span></span>

<span data-ttu-id="9dd82-105">Il tipo di enumerazione **WMDM \_ FORMATCODE** definisce un elenco di codici di formato che descrivono i tipi di contenuto trasferiti da e verso un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9dd82-105">The **WMDM\_FORMATCODE** enumeration type defines a list of format codes that describe types of content transferred to and from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd82-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9dd82-106">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="9dd82-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="9dd82-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9dd82-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM \_ FORMATCODE \_ abituata**</span><span class="sxs-lookup"><span data-stu-id="9dd82-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM\_FORMATCODE\_NOTUSED**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-109">Non viene utilizzato alcun codice di formato.</span><span class="sxs-lookup"><span data-stu-id="9dd82-109">No format code is used.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM \_ FORMATCODE \_ ALLIMAGES**</span><span class="sxs-lookup"><span data-stu-id="9dd82-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM\_FORMATCODE\_ALLIMAGES**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-111">Codice di formattazione che può essere utilizzato per eseguire una query per tutte le immagini.</span><span class="sxs-lookup"><span data-stu-id="9dd82-111">Format code that can be used to query for all images.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**FORMATCODE WMDM non \_ \_ definito**</span><span class="sxs-lookup"><span data-stu-id="9dd82-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM\_FORMATCODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-113">Codice del formato utilizzato per eseguire una query per tutti gli oggetti non definiti.</span><span class="sxs-lookup"><span data-stu-id="9dd82-113">Format code used to query for all undefined objects.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**\_associazione WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="9dd82-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM\_FORMATCODE\_ASSOCIATION**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-115">Codice del formato utilizzato per definire un collegamento tra due oggetti.</span><span class="sxs-lookup"><span data-stu-id="9dd82-115">Format code used to define a link between two objects.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**\_script WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="9dd82-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**WMDM\_FORMATCODE\_SCRIPT**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-117">Formattare il codice per un file di script.</span><span class="sxs-lookup"><span data-stu-id="9dd82-117">Format code for a script file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**\_ \_ eseguibile WMDM FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**WMDM\_FORMATCODE\_EXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-119">Formattare il codice per un file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="9dd82-119">Format code for an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**\_testo FORMATCODE \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="9dd82-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**WMDM\_FORMATCODE\_TEXT**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-121">Formattare il codice per un file di testo.</span><span class="sxs-lookup"><span data-stu-id="9dd82-121">Format code for a text file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM \_ FORMATCODE \_ HTML**</span><span class="sxs-lookup"><span data-stu-id="9dd82-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM\_FORMATCODE\_HTML**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-123">Formattare il codice per un file HTML.</span><span class="sxs-lookup"><span data-stu-id="9dd82-123">Format code for an HTML file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM \_ FORMATCODE \_ DPOF**</span><span class="sxs-lookup"><span data-stu-id="9dd82-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM\_FORMATCODE\_DPOF**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-125">Codice del formato utilizzato per rappresentare il formato dell'ordine di stampa digitale.</span><span class="sxs-lookup"><span data-stu-id="9dd82-125">Format code used to represent the digital print order format.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM \_ FORMATCODE \_ AIFF**</span><span class="sxs-lookup"><span data-stu-id="9dd82-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM\_FORMATCODE\_AIFF**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-127">Codice del formato utilizzato per rappresentare il formato del file di interscambio audio.</span><span class="sxs-lookup"><span data-stu-id="9dd82-127">Format code used to represent the audio interchange file format.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM \_ FORMATCODE \_ Wave**</span><span class="sxs-lookup"><span data-stu-id="9dd82-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM\_FORMATCODE\_WAVE**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-129">Codice di formattazione usato per un file WAV.</span><span class="sxs-lookup"><span data-stu-id="9dd82-129">Format code used for a WAV file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM \_ FORMATCODE \_ MP3**</span><span class="sxs-lookup"><span data-stu-id="9dd82-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM\_FORMATCODE\_MP3**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-131">Codice di formattazione usato per un file MP3.</span><span class="sxs-lookup"><span data-stu-id="9dd82-131">Format code used for an MP3 file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM \_ FORMATCODE \_ AVI**</span><span class="sxs-lookup"><span data-stu-id="9dd82-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM\_FORMATCODE\_AVI**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-133">Codice di formattazione usato per un file AVI.</span><span class="sxs-lookup"><span data-stu-id="9dd82-133">Format code used for an AVI file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM \_ FORMATCODE \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="9dd82-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM\_FORMATCODE\_MPEG**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-135">Codice di formattazione usato per un file MPEG.</span><span class="sxs-lookup"><span data-stu-id="9dd82-135">Format code used for an MPEG file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM \_ FORMATCODE \_ ASF**</span><span class="sxs-lookup"><span data-stu-id="9dd82-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM\_FORMATCODE\_ASF**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-137">Codice del formato utilizzato per rappresentare un file di formato di sistema avanzato (ASF).</span><span class="sxs-lookup"><span data-stu-id="9dd82-137">Format code used to represent an Advanced Systems Format (ASF) file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM \_ FORMATCODE \_ riservato per \_ primo**</span><span class="sxs-lookup"><span data-stu-id="9dd82-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM\_FORMATCODE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-139">Formattare il codice che è il primo in un intervallo riservato a PTP (Picture Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="9dd82-139">Format code that is the first in a range reserved for Picture Transfer Protocol (PTP).</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM \_ FORMATCODE \_ riservato per \_ ultimo**</span><span class="sxs-lookup"><span data-stu-id="9dd82-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM\_FORMATCODE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-141">Formattare il codice che è l'ultimo in un intervallo riservato per PTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-141">Format code that is last in a range reserved for PTP.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**\_immagine FORMATCODE WMDM non \_ \_ definita**</span><span class="sxs-lookup"><span data-stu-id="9dd82-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**WMDM\_FORMATCODE\_IMAGE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-143">Codice del formato utilizzato per rappresentare l'immagine di un tipo non definito.</span><span class="sxs-lookup"><span data-stu-id="9dd82-143">Format code used to represent and image of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM \_ FORMATCODE \_ Image \_ EXIF**</span><span class="sxs-lookup"><span data-stu-id="9dd82-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM\_FORMATCODE\_IMAGE\_EXIF**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-145">Formattare il codice per un file EXIF.</span><span class="sxs-lookup"><span data-stu-id="9dd82-145">Format code for an EXIF file.</span></span> <span data-ttu-id="9dd82-146">Usato anche per le immagini JPEG non coperte da WMDM \_ FORMATCODE \_ Image \_ JP2 o WMDM \_ FORMATCODE \_ Image \_ JPX.</span><span class="sxs-lookup"><span data-stu-id="9dd82-146">Also used for JPEG images not covered by WMDM\_FORMATCODE\_IMAGE\_JP2 or WMDM\_FORMATCODE\_IMAGE\_JPX.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM \_ FORMATCODE \_ Image \_ TIFFEP**</span><span class="sxs-lookup"><span data-stu-id="9dd82-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFEP**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-148">Codice di formattazione usato per le immagini di tipo Tagged Image File Format per la fotografia elettronica (TIFF/EP)</span><span class="sxs-lookup"><span data-stu-id="9dd82-148">Format code used for images that are of type Tagged Image File Format for Electronic Photography (TIFF/EP)</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM \_ FORMATCODE \_ Image \_ FlashPix**</span><span class="sxs-lookup"><span data-stu-id="9dd82-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM\_FORMATCODE\_IMAGE\_FLASHPIX**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-150">Formattare il codice per un file di tipo FPX.</span><span class="sxs-lookup"><span data-stu-id="9dd82-150">Format code for a file of type FPX.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM \_ \_ immagine \_ BMP FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM\_FORMATCODE\_IMAGE\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-152">Formattare il codice per un file di tipo BMP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-152">Format code for a file of type BMP.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM \_ FORMATCODE \_ Image \_ CIFF**</span><span class="sxs-lookup"><span data-stu-id="9dd82-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM\_FORMATCODE\_IMAGE\_CIFF**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-154">Formattare il codice per un'immagine nel formato di file dell'immagine della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="9dd82-154">Format code for an image in the camera image file format.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**\_ \_ gif immagine FORMATCODE \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="9dd82-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**WMDM\_FORMATCODE\_IMAGE\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-156">Formattare il codice per un file GIF.</span><span class="sxs-lookup"><span data-stu-id="9dd82-156">Format code for a GIF file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM \_ FORMATCODE \_ Image \_ JFIF**</span><span class="sxs-lookup"><span data-stu-id="9dd82-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM\_FORMATCODE\_IMAGE\_JFIF**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-158">Formattare il codice per un file di tipo JFIF.</span><span class="sxs-lookup"><span data-stu-id="9dd82-158">Format code for a file of type JFIF.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM \_ FORMATCODE \_ Image \_ PCD**</span><span class="sxs-lookup"><span data-stu-id="9dd82-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM\_FORMATCODE\_IMAGE\_PCD**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-160">Formattare il codice per un'immagine di tipo CD foto.</span><span class="sxs-lookup"><span data-stu-id="9dd82-160">Format code for an image of type photo cd.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM \_ FORMATCODE \_ Image \_ PICT**</span><span class="sxs-lookup"><span data-stu-id="9dd82-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM\_FORMATCODE\_IMAGE\_PICT**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-162">Formattare il codice per un'immagine di tipo PICT.</span><span class="sxs-lookup"><span data-stu-id="9dd82-162">Format code for an image of type PICT.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**\_ \_ png immagine WMDM \_ FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**WMDM\_FORMATCODE\_IMAGE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-164">Formattare il codice per un'immagine di tipo PNG.</span><span class="sxs-lookup"><span data-stu-id="9dd82-164">Format code for an image of type PNG.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**\_ \_ TIFF immagine FORMATCODE \_ WMDM**</span><span class="sxs-lookup"><span data-stu-id="9dd82-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-166">Formattare il codice per un file di tipo TIFF.</span><span class="sxs-lookup"><span data-stu-id="9dd82-166">Format code for a file of type TIFF.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM \_ FORMATCODE \_ Image \_ TIFFIT**</span><span class="sxs-lookup"><span data-stu-id="9dd82-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFIT**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-168">Formattare il codice per un'immagine di tipo Tagged Image File Format con la tecnologia di immagine.</span><span class="sxs-lookup"><span data-stu-id="9dd82-168">Format code for an image of type Tagged Image File Format with image technology.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM \_ FORMATCODE \_ Image \_ JP2**</span><span class="sxs-lookup"><span data-stu-id="9dd82-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM\_FORMATCODE\_IMAGE\_JP2**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-170">Formattare il codice per un'immagine JPEG200.</span><span class="sxs-lookup"><span data-stu-id="9dd82-170">Format code for a jpeg200 image.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**WMDM \_ FORMATCODE \_ Image \_ JPX**</span><span class="sxs-lookup"><span data-stu-id="9dd82-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**WMDM\_FORMATCODE\_IMAGE\_JPX**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-172">Formattare il codice per un'immagine basata su JPEG200, usando la registrazione di immagini ancora estese.</span><span class="sxs-lookup"><span data-stu-id="9dd82-172">Format code for an image built on JPEG200, using extended still image registration.</span></span> <span data-ttu-id="9dd82-173">L'estensione del nome file è in genere. JPF o. JPX.</span><span class="sxs-lookup"><span data-stu-id="9dd82-173">The file name extension is usually .jpf or .jpx.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**WMDM \_ FORMATCODE \_ Image \_ riservato per \_ primo**</span><span class="sxs-lookup"><span data-stu-id="9dd82-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-175">Formattare il codice che è il primo in un intervallo riservato per un riferimento a un'immagine in PTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-175">Format code that is the first in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**WMDM \_ FORMATCODE \_ Image \_ reserved \_ Last**</span><span class="sxs-lookup"><span data-stu-id="9dd82-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-177">Formattare il codice che rappresenta l'ultimo in un intervallo riservato per un riferimento a un'immagine in PTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-177">Format code that is the last in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDFIRMWARE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM\_FORMATCODE\_UNDEFINEDFIRMWARE**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-179">Formattare il codice quando il firmware non è definito.</span><span class="sxs-lookup"><span data-stu-id="9dd82-179">Format code when firmware is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**WMDM \_ \_WBMP FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span> **WMDM\_FORMATCODE\_WBMP**</span></span> 
</dt> <dd>

<span data-ttu-id="9dd82-181">Formattare il codice per un'immagine di bitmap Wireless Application Protocol (wbmp).</span><span class="sxs-lookup"><span data-stu-id="9dd82-181">Format code for a Wireless Application Protocol Bitmap (.wbmp) image.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**WMDM \_ \_JPEGXR FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span> **WMDM\_FORMATCODE\_JPEGXR**</span></span> 
</dt> <dd>

<span data-ttu-id="9dd82-183">Formattare il codice per un'immagine della foto HD</span><span class="sxs-lookup"><span data-stu-id="9dd82-183">Format code for an HD Photo image</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="9dd82-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-185">Formattare il codice per il formato di immagine Windows.</span><span class="sxs-lookup"><span data-stu-id="9dd82-185">Format code for Windows image format.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO**</span><span class="sxs-lookup"><span data-stu-id="9dd82-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM\_FORMATCODE\_UNDEFINEDAUDIO**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-187">Formattare il codice per un file audio di tipo non definito.</span><span class="sxs-lookup"><span data-stu-id="9dd82-187">Format code for an audio file of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM \_ FORMATCODE \_ WMA**</span><span class="sxs-lookup"><span data-stu-id="9dd82-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM\_FORMATCODE\_WMA**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-189">Formattare il codice per un file di Windows Media Audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="9dd82-189">Format code for a Windows Media Audio (WMA) file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM \_ FORMATCODE \_ OGG**</span><span class="sxs-lookup"><span data-stu-id="9dd82-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM\_FORMATCODE\_OGG**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-191">Formattare il codice per un file audio con codifica Vorbis in un contenitore Ogg.</span><span class="sxs-lookup"><span data-stu-id="9dd82-191">Format code for a Vorbis-encoded audio file in an Ogg container.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM \_ FORMATCODE \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="9dd82-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM\_FORMATCODE\_AAC**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-193">Formattare il codice per un file AAC (Advanced Audio Coding).</span><span class="sxs-lookup"><span data-stu-id="9dd82-193">Format code for an Advanced Audio Coding (AAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM \_ FORMATCODE \_ udibile**</span><span class="sxs-lookup"><span data-stu-id="9dd82-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM\_FORMATCODE\_AUDIBLE**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-195">Formattare il codice per un file acustico.</span><span class="sxs-lookup"><span data-stu-id="9dd82-195">Format code for an Audible file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM \_ FORMATCODE \_ FLAC**</span><span class="sxs-lookup"><span data-stu-id="9dd82-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM\_FORMATCODE\_FLAC**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-197">Formattare il codice per un file FLAC (lossless audio codec) gratuito.</span><span class="sxs-lookup"><span data-stu-id="9dd82-197">Format code for a Free Lossless Audio Codec (FLAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**WMDM \_ \_QCELP FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span> **WMDM\_FORMATCODE\_QCELP**</span></span> 
</dt> <dd>

<span data-ttu-id="9dd82-199">Codice di formattazione per un file di codec QCELP (codice Qualcomm Excited Linear Prediction).</span><span class="sxs-lookup"><span data-stu-id="9dd82-199">Format code for a Qualcomm Code Excited Linear Prediction (QCELP) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**WMDM \_ \_AMR FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span> **WMDM\_FORMATCODE\_AMR**</span></span> 
</dt> <dd>

<span data-ttu-id="9dd82-201">Formattare il codice per un file di codec AMR (Adaptive multirate audio).</span><span class="sxs-lookup"><span data-stu-id="9dd82-201">Format code for an Adaptive Multi-Rate audio (AMR) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO**</span><span class="sxs-lookup"><span data-stu-id="9dd82-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM\_FORMATCODE\_UNDEFINEDVIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-203">Formattare il codice per un file video con un tipo non definito.</span><span class="sxs-lookup"><span data-stu-id="9dd82-203">Format code for a video file with an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM \_ FORMATCODE \_ WMV**</span><span class="sxs-lookup"><span data-stu-id="9dd82-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM\_FORMATCODE\_WMV**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-205">Formattare il codice per un file di Windows Media Video (WMV).</span><span class="sxs-lookup"><span data-stu-id="9dd82-205">Format code for a Windows Media Video (WMV) file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM \_ FORMATCODE \_ MP4**</span><span class="sxs-lookup"><span data-stu-id="9dd82-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM\_FORMATCODE\_MP4**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-207">Formattare il codice per un file MP4.</span><span class="sxs-lookup"><span data-stu-id="9dd82-207">Format code for an MP4 file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM \_ FORMATCODE \_ MP2**</span><span class="sxs-lookup"><span data-stu-id="9dd82-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM\_FORMATCODE\_MP2**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-209">Formattare il codice per un file MP2.</span><span class="sxs-lookup"><span data-stu-id="9dd82-209">Format code for an MP2 file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**WMDM \_ FORMATCODE \_ 3G2**</span><span class="sxs-lookup"><span data-stu-id="9dd82-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span> **WMDM\_FORMATCODE\_3G2**</span></span> 
</dt> <dd>

<span data-ttu-id="9dd82-211">Formattare il codice per un formato del contenitore multimediale 3G2 (3GPP2).</span><span class="sxs-lookup"><span data-stu-id="9dd82-211">Format code for a 3G2 (3GPP2) multimedia container format.</span></span> <span data-ttu-id="9dd82-212">Un file di questo tipo può contenere audio, video o testo.</span><span class="sxs-lookup"><span data-stu-id="9dd82-212">A file of this type may contain audio, video, or text.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**WMDM \_ FORMATCODE \_ AVCHD**</span><span class="sxs-lookup"><span data-stu-id="9dd82-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span> **WMDM\_FORMATCODE\_AVCHD**</span></span> 
</dt> <dd>

<span data-ttu-id="9dd82-214">Formattare il codice per un file video AVCHD (Advanced Video Coding High Definition).</span><span class="sxs-lookup"><span data-stu-id="9dd82-214">Format code for an AVCHD (Advanced Video Coding High Definition) video file.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**WMDM \_ FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="9dd82-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span> **WMDM\_FORMATCODE\_ATSCTS**</span></span> 
</dt> <dd>

<span data-ttu-id="9dd82-216">Formattare il codice per lo standard del formato ATSCs (Advanced Television Systems Committee).</span><span class="sxs-lookup"><span data-stu-id="9dd82-216">Format code for the Advanced Television Systems Committee (ATSCTS) format standard.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**WMDM \_ \_DVBTS FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span> **WMDM\_FORMATCODE\_DVBTS**</span></span> 
</dt> <dd>

<span data-ttu-id="9dd82-218">Formattare il codice per un video MPEG-2 e MPEG-1 Layer II, oppure AC-3, audio all'interno di un flusso di trasporto MPEG-2 conforme a DVB.</span><span class="sxs-lookup"><span data-stu-id="9dd82-218">Format code for an MPEG-2 video and MPEG-1 Layer II, or AC-3, audio within a DVB-compliant MPEG-2 Transport Stream.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM \_ FORMATCODE \_ undefined**</span><span class="sxs-lookup"><span data-stu-id="9dd82-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM\_FORMATCODE\_UNDEFINEDCOLLECTION**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-220">Formattare il codice per una raccolta di un tipo non definito.</span><span class="sxs-lookup"><span data-stu-id="9dd82-220">Format code for a collection of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMULTIMEDIAALBUM**</span><span class="sxs-lookup"><span data-stu-id="9dd82-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTMULTIMEDIAALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-222">Formattare il codice per un album multimediale in cui l'oggetto contiene le proprietà di un album multimediale e, facoltativamente, i dati.</span><span class="sxs-lookup"><span data-stu-id="9dd82-222">Format code for a multimedia album where the object contains the properties of a multimedia album and, optionally, data.</span></span> <span data-ttu-id="9dd82-223">Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-223">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTIMAGEALBUM**</span><span class="sxs-lookup"><span data-stu-id="9dd82-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM\_FORMATCODE\_ABSTRACTIMAGEALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-225">Formattare il codice per un album di immagini in cui l'oggetto contiene le proprietà di un album di immagini e, facoltativamente, i dati.</span><span class="sxs-lookup"><span data-stu-id="9dd82-225">Format code for an image album where the object contains the properties of an image album and, optionally, data.</span></span> <span data-ttu-id="9dd82-226">Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-226">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTAUDIOALBUM**</span><span class="sxs-lookup"><span data-stu-id="9dd82-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-228">Formattare il codice per un album audio in cui l'oggetto contiene le proprietà di un album audio e, facoltativamente, i dati.</span><span class="sxs-lookup"><span data-stu-id="9dd82-228">Format code for an audio album where the object contains the properties of an audio album and, optionally, data.</span></span> <span data-ttu-id="9dd82-229">Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-229">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTVIDEOALBUM**</span><span class="sxs-lookup"><span data-stu-id="9dd82-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTVIDEOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-231">Formattare il codice per un album video in cui l'oggetto contiene le proprietà di un album video e, facoltativamente, i dati.</span><span class="sxs-lookup"><span data-stu-id="9dd82-231">Format code for a video album where the object contains the properties of a video album and, optionally, data.</span></span> <span data-ttu-id="9dd82-232">Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-232">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="9dd82-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-234">Formattare il codice per una playlist audio/video in cui l'oggetto contiene le proprietà di una playlist audio/video e, facoltativamente, i dati.</span><span class="sxs-lookup"><span data-stu-id="9dd82-234">Format code for an audio/video playlist where the object contains the properties of an audio/video playlist and, optionally, data.</span></span> <span data-ttu-id="9dd82-235">Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-235">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACTGROUP**</span><span class="sxs-lookup"><span data-stu-id="9dd82-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACTGROUP**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-237">Formattare il codice per un gruppo di contatti in cui l'oggetto contiene le proprietà di un gruppo di contatti e, facoltativamente, i dati.</span><span class="sxs-lookup"><span data-stu-id="9dd82-237">Format code for a contact group where the object contains the properties of a contact group and, optionally, data.</span></span> <span data-ttu-id="9dd82-238">Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-238">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGEFOLDER**</span><span class="sxs-lookup"><span data-stu-id="9dd82-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGEFOLDER**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-240">Formattare il codice per una cartella di messaggi in cui l'oggetto contiene le proprietà di una cartella del messaggio e, facoltativamente, i dati.</span><span class="sxs-lookup"><span data-stu-id="9dd82-240">Format code for a message folder where the object contains the properties of a message folder and, optionally, data.</span></span> <span data-ttu-id="9dd82-241">Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-241">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCHAPTEREDPRODUCTION**</span><span class="sxs-lookup"><span data-stu-id="9dd82-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM\_FORMATCODE\_ABSTRACTCHAPTEREDPRODUCTION**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-243">Formattare il codice per una produzione con capitolo in cui l'oggetto contiene le proprietà di una produzione con capitoli e, facoltativamente, i dati.</span><span class="sxs-lookup"><span data-stu-id="9dd82-243">Format code for a chaptered production where the object contains the properties of a chaptered production and, optionally, data.</span></span> <span data-ttu-id="9dd82-244">Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-244">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM \_ FORMATCODE \_ WPLPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="9dd82-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM\_FORMATCODE\_WPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-246">Formattare il codice per una playlist formattata con la formattazione Windows Media playlist.</span><span class="sxs-lookup"><span data-stu-id="9dd82-246">Format code for a playlist formatted with Windows Media playlist formatting.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM \_ FORMATCODE \_ M3UPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="9dd82-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM\_FORMATCODE\_M3UPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-248">Formattare il codice per una playlist con la formattazione M3U.</span><span class="sxs-lookup"><span data-stu-id="9dd82-248">Format code for a playlist with M3U formatting.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM \_ FORMATCODE \_ MPLPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="9dd82-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM\_FORMATCODE\_MPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-250">Formattare il codice per una playlist con formattazione MPL.</span><span class="sxs-lookup"><span data-stu-id="9dd82-250">Format code for a playlist with MPL formatting.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM \_ FORMATCODE \_ ASXPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="9dd82-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM\_FORMATCODE\_ASXPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-252">Formattare il codice per una playlist con formattazione ASX.</span><span class="sxs-lookup"><span data-stu-id="9dd82-252">Format code for a playlist with ASX formatting.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM \_ FORMATCODE \_ PLSPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="9dd82-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM\_FORMATCODE\_PLSPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-254">Formattare il codice per una playlist con la formattazione dei PLS.</span><span class="sxs-lookup"><span data-stu-id="9dd82-254">Format code for a playlist with PLS formatting.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="9dd82-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM\_FORMATCODE\_UNDEFINEDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-256">Formattare il codice per un documento di tipo non definito.</span><span class="sxs-lookup"><span data-stu-id="9dd82-256">Format code for a document of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM \_ FORMATCODE \_ ABSTRACTDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="9dd82-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM\_FORMATCODE\_ABSTRACTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-258">Formattare il codice per un documento in cui l'oggetto contiene le proprietà di un documento e, facoltativamente, i dati.</span><span class="sxs-lookup"><span data-stu-id="9dd82-258">Format code for a document where the object contains the properties of a document and, optionally, data.</span></span> <span data-ttu-id="9dd82-259">Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-259">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**\_XMLDOCUMENT WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="9dd82-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM\_FORMATCODE\_XMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-261">Formattare il codice per un documento XML.</span><span class="sxs-lookup"><span data-stu-id="9dd82-261">Format code for an XML document.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM \_ FORMATCODE \_ MICROSOFTWORDDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="9dd82-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM\_FORMATCODE\_MICROSOFTWORDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-263">Formattare il codice per un documento di Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="9dd82-263">Format code for a Microsoft Word document.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM \_ FORMATCODE \_ MHTCOMPILEDHTMLDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="9dd82-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM\_FORMATCODE\_MHTCOMPILEDHTMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-265">Formattare il codice per un documento HTML compilato.</span><span class="sxs-lookup"><span data-stu-id="9dd82-265">Format code for a compiled HTML document.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM \_ FORMATCODE \_ MICROSOFTEXCELSPREADSHEET**</span><span class="sxs-lookup"><span data-stu-id="9dd82-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM\_FORMATCODE\_MICROSOFTEXCELSPREADSHEET**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-267">Formattare il codice per un foglio di calcolo di Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="9dd82-267">Format code for a Microsoft Excel spreadsheet.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM \_ FORMATCODE \_ MICROSOFTPOWERPOINTDOCUMENT**</span><span class="sxs-lookup"><span data-stu-id="9dd82-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM\_FORMATCODE\_MICROSOFTPOWERPOINTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-269">Formattare il codice per un documento di Microsoft PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="9dd82-269">Format code for a Microsoft PowerPoint document.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM\_FORMATCODE\_UNDEFINEDMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-271">Formattare il codice per un messaggio di tipo non definito.</span><span class="sxs-lookup"><span data-stu-id="9dd82-271">Format code for a message of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-273">Formattare il codice per un messaggio in cui l'oggetto contiene le proprietà di un messaggio e, facoltativamente, i dati.</span><span class="sxs-lookup"><span data-stu-id="9dd82-273">Format code for a message where the object contains the properties of a message and, optionally, data.</span></span> <span data-ttu-id="9dd82-274">Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-274">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCONTACT**</span><span class="sxs-lookup"><span data-stu-id="9dd82-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM\_FORMATCODE\_UNDEFINEDCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-276">Formattare il codice per un contatto di tipo non definito.</span><span class="sxs-lookup"><span data-stu-id="9dd82-276">Format code for a contact of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACT**</span><span class="sxs-lookup"><span data-stu-id="9dd82-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-278">Formattare il codice per un contatto in cui l'oggetto contiene le proprietà di un contatto e, facoltativamente, i dati.</span><span class="sxs-lookup"><span data-stu-id="9dd82-278">Format code for a contact where the object contains the properties of a contact and, optionally, data.</span></span> <span data-ttu-id="9dd82-279">Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-279">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM \_ FORMATCODE \_ VCARD2**</span><span class="sxs-lookup"><span data-stu-id="9dd82-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM\_FORMATCODE\_VCARD2**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-281">Formattare il codice per una scheda elettronica con la formattazione di vCard versione 2.</span><span class="sxs-lookup"><span data-stu-id="9dd82-281">Format code for an electronic card with vcard version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM \_ FORMATCODE \_ VCARD3**</span><span class="sxs-lookup"><span data-stu-id="9dd82-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM\_FORMATCODE\_VCARD3**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-283">Formattare il codice per una scheda elettronica con la formattazione di vCard versione 3.</span><span class="sxs-lookup"><span data-stu-id="9dd82-283">Format code for an electronic card with vcard version 3 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCALENDARITEM**</span><span class="sxs-lookup"><span data-stu-id="9dd82-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM\_FORMATCODE\_UNDEFINEDCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-285">Formattare il codice per un elemento del calendario elettronico di tipo non definito.</span><span class="sxs-lookup"><span data-stu-id="9dd82-285">Format code for an electronic calendar item of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCALENDARITEM**</span><span class="sxs-lookup"><span data-stu-id="9dd82-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM\_FORMATCODE\_ABSTRACTCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-287">Formattare il codice per un elemento del calendario in cui l'oggetto contiene le proprietà di un elemento del calendario e, facoltativamente, i dati.</span><span class="sxs-lookup"><span data-stu-id="9dd82-287">Format code for a calendar item where the object contains the properties of a calendar item and, optionally, data.</span></span> <span data-ttu-id="9dd82-288">Tutti i dati contenuti sono di un formato non definito rispetto alla specifica MTP.</span><span class="sxs-lookup"><span data-stu-id="9dd82-288">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM \_ FORMATCODE \_ VCALENDAR1**</span><span class="sxs-lookup"><span data-stu-id="9dd82-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM\_FORMATCODE\_VCALENDAR1**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-290">Formattare il codice per un elemento del calendario elettronico con la formattazione della versione 1 di vCalendar.</span><span class="sxs-lookup"><span data-stu-id="9dd82-290">Format code for an electronic calendar item with vcalendar version 1 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM \_ FORMATCODE \_ VCALENDAR2**</span><span class="sxs-lookup"><span data-stu-id="9dd82-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM\_FORMATCODE\_VCALENDAR2**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-292">Formattare il codice per un elemento del calendario elettronico con la formattazione vCalendar versione 2.</span><span class="sxs-lookup"><span data-stu-id="9dd82-292">Format code for an electronic calendar item with vcalendar version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDWINDOWSEXECUTABLE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM\_FORMATCODE\_UNDEFINEDWINDOWSEXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-294">Formattare il codice per un eseguibile basato su Windows di tipo non definito.</span><span class="sxs-lookup"><span data-stu-id="9dd82-294">Format code for a Windows-based executable of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**\_ \_ cast multimediale WMDM \_ FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM\_FORMATCODE\_MEDIA\_CAST**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-296">Formattare il codice per un oggetto cast multimediale.</span><span class="sxs-lookup"><span data-stu-id="9dd82-296">Format code for a media cast object.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**\_sezione WMDM FORMATCODE \_**</span><span class="sxs-lookup"><span data-stu-id="9dd82-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**WMDM\_FORMATCODE\_SECTION**</span></span>
</dt> <dd>

<span data-ttu-id="9dd82-298">Formattare il codice per una sezione di dati contenuta in un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="9dd82-298">Format code for a section of data that is contained in another object.</span></span>

</dd> <dt>

<span data-ttu-id="9dd82-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**WMDM \_ \_3G2A FORMATCODE**</span><span class="sxs-lookup"><span data-stu-id="9dd82-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span> **WMDM\_FORMATCODE\_3G2A**</span></span> 
</dt> <dd>

<span data-ttu-id="9dd82-300">Formattare il codice per un formato di contenitore multimediale 3G2A (3GPP2A).</span><span class="sxs-lookup"><span data-stu-id="9dd82-300">Format code for a 3G2A (3GPP2A) multimedia container format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9dd82-301">Commenti</span><span class="sxs-lookup"><span data-stu-id="9dd82-301">Remarks</span></span>

<span data-ttu-id="9dd82-302">Per individuare i formati supportati da un dispositivo, un'applicazione può usare [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) per eseguire query sulla proprietà del dispositivo **g \_ wszWMDMFormatsSupported** .</span><span class="sxs-lookup"><span data-stu-id="9dd82-302">To discover the formats supported by a device, an application can use [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to query the **g\_wszWMDMFormatsSupported** device property.</span></span>

<span data-ttu-id="9dd82-303">Per individuare le funzionalità del dispositivo per un particolare formato, un'applicazione può chiamare [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span><span class="sxs-lookup"><span data-stu-id="9dd82-303">To discover device capabilities for a particular format, an application can call [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span>

<span data-ttu-id="9dd82-304">Un'applicazione può impostare il codice di formato durante la creazione di una risorsa di archiviazione nel dispositivo includendo la proprietà **g \_ wszWMDMFormatCode** nei metadati passati nel parametro *pMetaData* di una chiamata a [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span><span class="sxs-lookup"><span data-stu-id="9dd82-304">An application can set the format code while creating a storage on device by including the **g\_wszWMDMFormatCode** property in metadata passed in the *pMetaData* parameter of a call to [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span></span>

<span data-ttu-id="9dd82-305">Un'applicazione può eseguire una query sul codice del formato di un'archiviazione chiamando [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) e recuperando la proprietà **g \_ wszWMDMFormatCode** .</span><span class="sxs-lookup"><span data-stu-id="9dd82-305">An application can query the format code of a storage by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) and retrieving the **g\_wszWMDMFormatCode** property.</span></span>

<span data-ttu-id="9dd82-306">Se il dispositivo supporta l'impostazione del codice del formato dopo la creazione dello spazio di archiviazione, un'applicazione può usare [**IWMDMStorage3::**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) SetProperty per impostare la proprietà **g \_ wszWMDMFormatCode** .</span><span class="sxs-lookup"><span data-stu-id="9dd82-306">If the device supports setting the format code after the creation of storage, an application can use [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) to set the **g\_wszWMDMFormatCode** property.</span></span> <span data-ttu-id="9dd82-307">Alcuni dispositivi potrebbero non consentire la modifica del codice del formato dopo la creazione dell'archiviazione nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9dd82-307">Some devices may not allow changing the format code after the storage is created on the device.</span></span> <span data-ttu-id="9dd82-308">Pertanto, è consigliabile impostare questa proprietà insieme ai metadati passati in [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) .</span><span class="sxs-lookup"><span data-stu-id="9dd82-308">Therefore, setting this property along with the metadata passed in [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) is strongly recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd82-309">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9dd82-309">Requirements</span></span>



| <span data-ttu-id="9dd82-310">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dd82-310">Requirement</span></span> | <span data-ttu-id="9dd82-311">Valore</span><span class="sxs-lookup"><span data-stu-id="9dd82-311">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd82-312">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9dd82-312">Header</span></span><br/> | <dl> <span data-ttu-id="9dd82-313"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9dd82-313"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dd82-314">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9dd82-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd82-315">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="9dd82-315">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="9dd82-316">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="9dd82-316">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="9dd82-317">**IWMDMDevice3:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="9dd82-317">**IWMDMDevice3::GetProperty**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[<span data-ttu-id="9dd82-318">**IWMDMStorage3:: GetMetadata**</span><span class="sxs-lookup"><span data-stu-id="9dd82-318">**IWMDMStorage3::GetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[<span data-ttu-id="9dd82-319">**IWMDMStorage3:: tometadata**</span><span class="sxs-lookup"><span data-stu-id="9dd82-319">**IWMDMStorage3::SetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[<span data-ttu-id="9dd82-320">**IWMDMStorage4::GetSpecifiedMetadata**</span><span class="sxs-lookup"><span data-stu-id="9dd82-320">**IWMDMStorage4::GetSpecifiedMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[<span data-ttu-id="9dd82-321">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="9dd82-321">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[<span data-ttu-id="9dd82-322">**Costanti dei metadati**</span><span class="sxs-lookup"><span data-stu-id="9dd82-322">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 





