---
description: I dispositivi portatili Windows supportano le proprietà immagine seguenti.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Proprietà immagine (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 959a008d9c30991058226e52db6e45ed417ee6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333523"
---
# <a name="image-properties"></a>Proprietà immagine

I dispositivi portatili Windows supportano le proprietà immagine seguenti.



| Proprietà                                                                                                                                       | VarType     | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **immagine di WPD \_ \_ BITDEPTH**                                                                                                                       | **\_UI4 VT** | Profondità di bit dell'immagine.                                                                                                                                                                                                                                                                                                                     |
| <span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**\_ \_ \_ stato correzione colore immagine \_ WPD** | **\_UI4 VT** | Enumerazione [**\_ \_ \_ \_ dei valori di stato con correzione del colore WPD**](wpd-color-corrected-status-values.md) che specifica se il file è stato con correzione del colore. In questo modo si impedisce a più dispositivi di correggere automaticamente il colore dell'immagine durante la post-elaborazione.<br/>                                                                       |
| **\_ \_ stato ritagliato immagine WPD \_**                                                                                                                | **\_UI4 VT** | Enumerazione [**\_ \_ \_ dei valori di stato ritagliata WPD**](wpd-cropped-status-values.md) che specifica se il file è stato ritagliato. In questo modo si impedisce a più dispositivi di ritagliare automaticamente l'immagine durante la post-elaborazione.<br/>                                                                                                        |
| **\_indice di \_ esposizione \_ Immagini WPD**                                                                                                                | **\_UI4 VT** | Valore che identifica le impostazioni della velocità della pellicola quando l'immagine è stata acquisita. Le impostazioni corrispondono alle designazioni ISO di ASA/DIN.<br/> In genere, un dispositivo supporta valori enumerati discreti, ma è possibile il controllo continuo su un intervallo.<br/> Il valore 0xFFFFFFFF corrisponde all'impostazione ISO automatica.<br/> |
| **WPD \_ \_ tempo di esposizione immagine \_**                                                                                                                 | **\_UI4 VT** | Identifica la velocità dell'otturatore del dispositivo quando l'immagine è stata acquisita. Le unità sono in secondi ridimensionate di 10000.<br/>                                                                                                                                                                                                                        |
| **immagine di WPD \_ \_ FNUMBER**                                                                                                                        | **\_UI4 VT** | Identifica l'impostazione di apertura della lente quando l'immagine è stata acquisita. Le unità sono uguali al numero f ridimensionato di 100.<br/>                                                                                                                                                                                                              |
| **\_ \_ risoluzione orizzontale immagine \_ WPD**                                                                                                         | **VT \_ R8**  | Indica la risoluzione orizzontale di un'immagine, espressa in punti per pollice (DPI).                                                                                                                                                                                                                                                                       |
| **\_ \_ risoluzione verticale dell'immagine WPD \_**                                                                                                           | **VT \_ R8**  | Indica la risoluzione verticale di un'immagine, espressa in punti per pollice (DPI).                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




