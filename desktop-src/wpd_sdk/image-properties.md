---
description: Windows Dispositivi portatili supporta le proprietà dell'immagine seguenti.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Proprietà immagine (PortableDevice.h)
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
ms.openlocfilehash: 0d2ebe552a66dadf6b9bec6a0a741d85e1c7f1f018ef108e36ec1bb3cb4b6165
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430760"
---
# <a name="image-properties"></a>Proprietà immagine

Windows Dispositivi portatili supporta le proprietà dell'immagine seguenti.



| Proprietà                                                                                                                                       | VarType     | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_BITDEPTH IMMAGINE \_ WPD**                                                                                                                       | **Interfaccia utente \_ VT4** | Profondità in bit dell'immagine.                                                                                                                                                                                                                                                                                                                     |
| <span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**STATO CORRETTO DEL COLORE \_ \_ \_ DELL'IMMAGINE WPD \_** | **Interfaccia utente \_ VT4** | Enumerazione [**WPD \_ COLOR \_ CORRECTED STATUS \_ \_ VALUES**](wpd-color-corrected-status-values.md) che specifica se il file è stato corretto a colori. Ciò impedisce a più dispositivi di correggere automaticamente il colore dell'immagine durante la post-elaborazione.<br/>                                                                       |
| **STATO RITAGLIATO DELL'IMMAGINE WPD \_ \_ \_**                                                                                                                | **Interfaccia utente \_ VT4** | Enumerazione [**WPD \_ CROPPED \_ STATUS \_ VALUES**](wpd-cropped-status-values.md) che specifica se il file è stato ritagliato. Ciò impedisce a più dispositivi di ritagliare automaticamente l'immagine durante la post-elaborazione.<br/>                                                                                                        |
| **INDICE DI ESPOSIZIONE DELLE IMMAGINI WPD \_ \_ \_**                                                                                                                | **Interfaccia utente \_ VT4** | Valore che identifica le impostazioni di velocità del film quando è stata acquisita l'immagine. Le impostazioni corrispondono alle designazioni ISO di ASA/DIN.<br/> In genere, un dispositivo supporta valori enumerati discreti, ma è possibile un controllo continuo su un intervallo.<br/> Il valore 0xFFFFFFFF corrisponde all'impostazione ISO automatica.<br/> |
| **TEMPO DI ESPOSIZIONE DELL'IMMAGINE WPD \_ \_ \_**                                                                                                                 | **Interfaccia utente \_ VT4** | Identifica la velocità di chiusura del dispositivo quando è stata acquisita l'immagine. Le unità vengono ridimensionate in secondi di 10000.<br/>                                                                                                                                                                                                                        |
| **FNUMBER \_ IMMAGINE WPD \_**                                                                                                                        | **Interfaccia utente \_ VT4** | Identifica l'impostazione di apertura dell'obiettivo quando è stata acquisita l'immagine. Le unità sono uguali al numero f ridimensionato di 100.<br/>                                                                                                                                                                                                              |
| **RISOLUZIONE ORIZZONTALE \_ DELL'IMMAGINE WPD \_ \_**                                                                                                         | **VT \_ R8**  | Indica la risoluzione orizzontale di un'immagine, in punti per pollice (DPI).                                                                                                                                                                                                                                                                       |
| **RISOLUZIONE VERTICALE \_ DELL'IMMAGINE WPD \_ \_**                                                                                                           | **VT \_ R8**  | Indica la risoluzione verticale di un'immagine, in punti per pollice (DPI).                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




