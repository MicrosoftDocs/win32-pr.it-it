---
title: DRM_Rights
description: La proprietà Diritti DRM specifica i diritti che l'applicazione richiederà al \_ successivo tentativo di aprire un file protetto.
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights windows Media Format
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d655ea3f4a0a5dccc8b5e1380296948c9a55dce1d86336f824b30189f6557d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930901"
---
# <a name="drm_rights"></a>Diritti \_ DRM

La **proprietà \_ Diritti DRM** specifica i diritti che l'applicazione richiederà al successivo tentativo di aprire un file protetto.

## <a name="global-constant"></a>Costante globale

g \_ wszWMDRM \_ Rights

## <a name="data-type"></a>Tipo di dati

**STRINGA DI \_ TIPO \_ WMT**

## <a name="remarks"></a>Commenti

Si tratta di una proprietà di lettura/scrittura recuperata tramite [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) e impostata usando [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) o [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

Nella tabella seguente sono elencati i diritti supportati.



| Destra                                           | Valore letterale stringa      | Descrizione                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ RIGHT \_ BACKUP                      | "Backup"            | Diritto di eseguire il backup della licenza.                                                                                                                                                                                        |
| g \_ wszWMDRM \_ RIGHT COLLABORATIVE \_ \_ PLAY         | "CollaborativePlay" | Diritto di riprodurre il file come parte di una playlist collaborativa.                                                                                                                                                          |
| g \_ wszWMDRM \_ RIGHT \_ COPY                        | "Copy"              | Diritto di copiare il file in un dispositivo. Questo diritto sostituisce i diritti di copia precedenti (g \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ CD, g \_ wszWMDRM \_ RIGHT COPY TO NON \_ \_ SDMI DEVICE e g \_ \_ \_ \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ SDMI \_ DEVICE). |
| g \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ CD                | "Print.redbook"     | Diritto di copiare il file in un CD (formato Red Book). In Windows Media DRM 10, questo diritto viene sostituito da g \_ wszWMDRM \_ RIGHT \_ COPY.<br/>                                                                             |
| g \_ wszWMDRM \_ RIGHT COPY TO NON \_ \_ \_ \_ \_ SDMI DEVICE | "Transfer.NONSDMI"  | Diritto di copiare il file in un dispositivo non SDMI. In Windows Media DRM 10, questo diritto viene sostituito da g \_ wszWMDRM \_ RIGHT \_ COPY.<br/>                                                                                  |
| g \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ SDMI \_ DEVICE      | "Transfer.SDMI"     | Diritto di copiare il file in un dispositivo conforme a SDMI. In Windows Media DRM 10, questo diritto viene sostituito da g \_ wszWMDRM \_ RIGHT \_ COPY.<br/>                                                                           |
| g \_ wszWMDRM \_ RIGHT \_ PLAYBACK                    | "Play"              | Diritto di riprodurre il file multimediale.                                                                                                                                                                                        |



 

Questa proprietà contiene una stringa di caratteri wide di uno o più diritti separati da punti e virgola, ad esempio: L"Playback; Copia; CollaborativePlay".

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 





