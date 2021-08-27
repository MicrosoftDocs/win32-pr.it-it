---
description: L'enumerazione MXDC S0 PAGE ENUMS viene usata per specificare i tipi di risorse che possono essere associate alle pagine nei documenti XPS e che possono essere elaborate o passate non elaborate da \_ \_ Microsoft \_ XPS Document Converter (MXDC) al relativo output.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: MXDC_S0_PAGE_ENUMS enumerazione (Winspool.h)
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
ms.openlocfilehash: 3aa6622ea65e00c1447e6042a41c998e9ab30a29d1172d43e1a1da81feb34c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471316"
---
# <a name="mxdc_s0_page_enums-enumeration"></a>Enumerazione MXDC \_ S0 \_ PAGE \_ ENUMS

L'enumerazione **MXDC \_ S0 \_ PAGE \_ ENUMS** viene usata per specificare i tipi di risorse che possono essere associate alle pagine nei documenti XPS e che possono essere elaborate o passate non elaborate da Microsoft XPS Document Converter (MXDC) al relativo output.

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

<span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC \_ RESOURCE \_ TTF**
</dt> <dd>

Tipo di carattere TrueType o OpenType.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC \_ RESOURCE \_ JPEG**
</dt> <dd>

Immagine JPEG

</dd> <dt>

<span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC \_ RESOURCE \_ PNG**
</dt> <dd>

Immagine PNG.

</dd> <dt>

<span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**TIFF \_ DELLA RISORSA \_ MXDC**
</dt> <dd>

Immagine TIFF.

</dd> <dt>

<span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**WDP \_ DELLA RISORSA \_ MXDC**
</dt> <dd>

Windows Immagine foto multimediale.

</dd> <dt>

<span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**DIZIONARIO RISORSE \_ \_ MXDC**
</dt> <dd>

Dizionario risorse remote che deve essere passato all'output di MXDC non elaborato.

</dd> <dt>

<span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**PROFILO \_ ICC DELLA \_ RISORSA \_ MXDC**
</dt> <dd>

Profilo ICC che deve essere passato all'output di MXDC non elaborato.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**ANTEPRIMA \_ JPEG DELLA \_ RISORSA MXDC \_**
</dt> <dd>

Anteprima JPEG che deve essere passata all'output di MXDC non elaborato.

</dd> <dt>

<span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**ANTEPRIMA \_ \_ PNG DELLA RISORSA MXDC \_**
</dt> <dd>

Anteprima PNG che deve essere passata all'output di MXDC non elaborato.

</dd> <dt>

<span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC \_ RESOURCE \_ MAX**
</dt> <dd>

Numero massimo di risorse per la convalida.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene usata principalmente come membro **dwResourceType** della [**struttura MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T.**](mxdcxpss0pageresource.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



 

 




