---
title: Profili di sistema localizzati
description: Profili di sistema localizzati
ms.assetid: 2c218ab4-ecdb-414c-aa42-b71a42e340e5
keywords:
- Windows Media Format SDK, profili di sistema
- Advanced Systems Format (ASF), profili di sistema
- ASF (Advanced Systems Format),profili di sistema
- Windows Media Format SDK, profili di sistema localizzati
- Advanced Systems Format (ASF), profili di sistema localizzati
- ASF (Advanced Systems Format), profili di sistema localizzati
- profili di sistema, localizzati
- profili di sistema localizzati, elenco di
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe3ca0abbe0e5b92645f6adaa1f6ebfdc44d52064d6fb8e1389420d19651b7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707711"
---
# <a name="localized-system-profiles"></a>Profili di sistema localizzati

Nella tabella seguente sono elencati i file del profilo di sistema localizzati inclusi in Windows Media Format SDK e le lingue associate a ognuno. Questi file vengono installati nella \[ cartella SDKRoot \] \\ WMSDK \\ WMFSDK9 \\ LocalizedProfiles. Per accedere a un file specifico con i **metodi IWMProfileManagerLanguage,** è necessario spostarlo nella directory radice del sistema insieme ai file del profilo di sistema predefiniti.



| Linguaggio              | Nome file    |
|-----------------------|--------------|
| Arabo                | WMPrfAra.prx |
| Cinese semplificato  | WMPrfCHS.prx |
| Cinese tradizionale | WMPrfCHT.prx |
| Ceco                 | WMPrfCsy.prx |
| Danese                | WMPrfDan.prx |
| Olandese                 | WMPrfNld.prx |
| Finlandese               | WMPrfFin.prx |
| Francese                | WMPrfFra.prx |
| Tedesco                | WMPrfDeu.prx |
| Greco                 | WMPrfEll.prx |
| Ebraico                | WMPrfHeb.prx |
| Ungherese             | WMPrfHun.prx |
| Italiano               | WMPrfIta.prx |
| Giapponese              | WMPrfJpn.prx |
| Coreano                | WMPrfKor.prx |
| Norvegese             | WMPrfNor.prx |
| Polacco                | WMPrfPlk.prx |
| Portoghese (Brasile)   | WMPrfPtb.prx |
| Portoghese (Portogallo) | WMPrfPtg.prx |
| Russo               | WMPrfRus.prx |
| Slovacco                | WMPrfSky.prx |
| Sloveno             | WMPrfSlv.prx |
| Spagnolo               | WMPrfEsp.prx |
| Svedese               | WMPrfSve.prx |
| Turco               | WMPrfTrk.prx |



 

È possibile impostare la lingua per l'oggetto profile manager chiamando il [**metodo IWMProfileManagerLanguage::SetUserLanguageID.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanagerlanguage-setuserlanguageid) Per la maggior parte delle lingue, viene esaminato solo l'identificatore di lingua principale in LANGID. Le eccezioni sono per le lingue cinese e portoghese, in cui viene usato anche l'identificatore della lingua secondaria. Nella tabella seguente viene illustrato come creare un LANGID da specificare nel **metodo SetUserLanguageID.**



| Lingua primaria-secondaria | MAKELANGID Macro                                             |
|----------------------------|--------------------------------------------------------------|
| Cinese (semplificato)       | MAKELANGID( LANG \_ CHINESE, SUBLANG \_ CHINESE \_ SIMPLIFIED)     |
| Cinese (tradizionale)      | MAKELANGID( LANG \_ CHINESE, SUBLANG \_ CHINESE \_ SINGAPORE)      |
| Portoghese (Brasile)        | MAKELANGID(LANG \_ PORTOGHESE, SUBLANG \_ PORTOGHESE \_ BRASILIANO) |
| Portoghese (Portogallo)      | MAKELANGID(LANG \_ PORTOGHESE, SUBLANG \_ PORTOGHESE)            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> <dt>

[**Profili di sistema**](system-profiles.md)
</dt> </dl>

 

 




