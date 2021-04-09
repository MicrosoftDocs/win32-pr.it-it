---
description: L' \_ enumerazione MXDC S0 \_ Page \_ Enumerations viene utilizzata per specificare i tipi di risorse che possono essere associati alle pagine nei documenti XPS e che possono essere elaborati, o passati non elaborati, da Microsoft XPS Document Converter (MXDC) all'output.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: Enumerazione MXDC_S0_PAGE_ENUMS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1b4331210027f7fc23f36fb6b9d13a2c232ccbf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881602"
---
# <a name="mxdc_s0_page_enums-enumeration"></a>Enumerazione enumerazioni della \_ pagina S0 MXDC \_ \_

L'enumerazione **MXDC \_ S0 \_ Page \_ Enumerations** viene utilizzata per specificare i tipi di risorse che possono essere associati alle pagine nei documenti XPS e che possono essere elaborati, o passati non elaborati, da Microsoft XPS Document Converter (MXDC) all'output.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**\_ttf risorse \_ MXDC**
</dt> <dd>

Tipo di carattere TrueType o OpenType.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC di \_ risorse \_ JPEG**
</dt> <dd>

Immagine JPEG

</dd> <dt>

<span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**\_png risorse \_ MXDC**
</dt> <dd>

Immagine PNG.

</dd> <dt>

<span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**\_TIFF risorse \_ MXDC**
</dt> <dd>

Immagine TIFF.

</dd> <dt>

<span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**\_WDP risorse \_ MXDC**
</dt> <dd>

Immagine foto di Windows Media.

</dd> <dt>

<span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**\_dizionario risorse \_ MXDC**
</dt> <dd>

Dizionario risorse remoto da passare all'output di MXDC non elaborato.

</dd> <dt>

<span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**\_ \_ profilo ICC della risorsa MXDC \_**
</dt> <dd>

Profilo ICC da passare all'output di MXDC non elaborato.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**\_ \_ Anteprima JPEG risorsa \_ MXDC**
</dt> <dd>

Anteprima JPEG da passare all'output di MXDC non elaborato.

</dd> <dt>

<span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**\_ \_ Anteprima png risorse \_ MXDC**
</dt> <dd>

Anteprima PNG da passare all'output di MXDC non elaborato.

</dd> <dt>

<span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC \_ risorsa \_ massima**
</dt> <dd>

Numero massimo di risorse per la convalida.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata principalmente come membro **dwResourceType** della struttura della [**\_ \_ \_ risorsa \_ T MXDC XPS S0PAGE**](mxdcxpss0pageresource.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |



 

 




