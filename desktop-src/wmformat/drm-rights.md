---
title: DRM_Rights
description: La \_ Proprietà diritti DRM specifica i diritti che l'applicazione richiederà nel tentativo successivo di aprire un file protetto.
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights formato Windows Media
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542e511c11111bb2698d9c936a1f0973a2145c9b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046288"
---
# <a name="drm_rights"></a>\_Diritti DRM

La **proprietà \_ diritti DRM** specifica i diritti che l'applicazione richiederà nel tentativo successivo di aprire un file protetto.

## <a name="global-constant"></a>Costante globale

\_diritti g wszWMDRM \_

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Si tratta di una proprietà di lettura/scrittura che viene recuperata utilizzando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) e impostata utilizzando [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) o [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

Nella tabella seguente sono elencati i diritti supportati.



| Destra                                           | Valore letterale stringa      | Descrizione                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ right \_ backup                      | Backup            | Diritto di eseguire il backup della licenza.                                                                                                                                                                                        |
| g \_ wszWMDRM \_ right \_ collaborative \_ Play         | "CollaborativePlay" | Diritto di riprodurre il file come parte di una playlist collaborativa.                                                                                                                                                          |
| g \_ wszWMDRM \_ \_ copia destra                        | "Copy"              | Diritto di copiare il file in un dispositivo. Questo diritto sostituisce i precedenti diritti di copia (g \_ wszWMDRM \_ right \_ copy \_ to \_ CD, g \_ wszWMDRM \_ right \_ copy \_ to \_ non \_ SDMI \_ Device e g \_ wszWMDRM \_ right copy \_ \_ to \_ SDMI \_ Device). |
| g \_ wszWMDRM \_ la \_ copia corretta \_ su \_ CD                | "Print. Redbook"     | Diritto di copiare il file in un CD (formato di libro rosso). In Windows Media DRM 10, questo diritto viene sostituito da g \_ wszWMDRM \_ right \_ Copy.<br/>                                                                             |
| g \_ wszWMDRM \_ la \_ copia destra \_ in un \_ \_ dispositivo non SDMI \_ | "Transfer. NONSDMI"  | Diritto di copiare il file in un dispositivo non SDMI. In Windows Media DRM 10, questo diritto viene sostituito da g \_ wszWMDRM \_ right \_ Copy.<br/>                                                                                  |
| g \_ wszWMDRM \_ la \_ Copia \_ destra \_ nel \_ dispositivo SDMI      | "Transfer. SDMI"     | Diritto di copiare il file in un dispositivo conforme a SDMI. In Windows Media DRM 10, questo diritto viene sostituito da g \_ wszWMDRM \_ right \_ Copy.<br/>                                                                           |
| g \_ wszWMDRM \_ riproduzione a destra \_                    | Play              | Diritto di riprodurre il file multimediale.                                                                                                                                                                                        |



 

Questa proprietà contiene una stringa di caratteri wide di uno o più diritti separati da punti e virgola, ad esempio: L "playback; Copia CollaborativePlay".

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> </dl>

 

 





