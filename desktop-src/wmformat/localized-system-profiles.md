---
title: Profili di sistema localizzati
description: Profili di sistema localizzati
ms.assetid: 2c218ab4-ecdb-414c-aa42-b71a42e340e5
keywords:
- Windows Media Format SDK, profili di sistema
- ASF (Advanced Systems Format), profili di sistema
- ASF (formato avanzato dei sistemi), profili di sistema
- Windows Media Format SDK, profili di sistema localizzati
- ASF (Advanced Systems Format), profili di sistema localizzati
- ASF (Advanced Systems Format), profili di sistema localizzati
- profili di sistema, localizzati
- profili di sistema localizzati, elenco di
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aaeecdf1d1d62d78df18e0ac1c5bffbf39f9778
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046264"
---
# <a name="localized-system-profiles"></a>Profili di sistema localizzati

Nella tabella seguente sono elencati i file di profilo di sistema localizzati inclusi in Windows Media Format SDK e le lingue associate a ciascuna di esse. Questi file vengono installati nella \[ cartella sdkroot \] \\ WMSDK \\ WMFSDK9 \\ LocalizedProfiles Per accedere a un file specifico con i metodi **IWMProfileManagerLanguage** , è necessario spostarlo nella directory radice del sistema insieme ai file del profilo di sistema predefiniti.



| Linguaggio              | Nome file    |
|-----------------------|--------------|
| Arabo                | WMPrfAra. prx |
| Cinese (semplificato)  | WMPrfCHS. prx |
| Cinese (tradizionale) | WMPrfCHT. prx |
| Ceco                 | WMPrfCsy. prx |
| Danese                | WMPrfDan. prx |
| Olandese                 | WMPrfNld. prx |
| Finlandese               | WMPrfFin. prx |
| Francese                | WMPrfFra. prx |
| Tedesco                | WMPrfDeu. prx |
| Greco                 | WMPrfEll. prx |
| Ebraico                | WMPrfHeb. prx |
| Ungherese             | WMPrfHun. prx |
| Italiano               | WMPrfIta. prx |
| Giapponese              | WMPrfJpn. prx |
| Coreano                | WMPrfKor. prx |
| Norvegese             | WMPrfNor. prx |
| Polacco                | WMPrfPlk. prx |
| Portoghese (Brasile)   | WMPrfPtb. prx |
| Portoghese (Portogallo) | WMPrfPtg. prx |
| Russo               | WMPrfRus. prx |
| Slovacco                | WMPrfSky. prx |
| Sloveno             | WMPrfSlv. prx |
| Spagnolo               | WMPrfEsp. prx |
| Svedese               | WMPrfSve. prx |
| Turco               | WMPrfTrk. prx |



 

È possibile impostare la lingua per l'oggetto di gestione del profilo chiamando il metodo [**IWMProfileManagerLanguage:: SetUserLanguageID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanagerlanguage-setuserlanguageid) . Per la maggior parte delle lingue, viene esaminato solo l'identificatore della lingua principale nella LANGID. Le eccezioni sono per le lingue cinese e portoghese, in cui viene utilizzato anche l'identificatore della lingua secondaria. La tabella seguente illustra come creare un LANGID da specificare nel metodo **SetUserLanguageID** .



| Primario-lingua secondaria | MAKELANGID (macro)                                             |
|----------------------------|--------------------------------------------------------------|
| Cinese (semplificato)       | MAKELANGID (LANG \_ cinese, \_ lingua cinese \_ semplificata)     |
| Cinese (tradizionale)      | MAKELANGID (LANG \_ cinese, SUBLANG \_ Chinese \_ )      |
| Portoghese (Brasile)        | MAKELANGID (LANG \_ portoghese, SUBLANG \_ Portoghese \_ brasiliano) |
| Portoghese (Portogallo)      | MAKELANGID (LANG \_ portoghese, SUBLANG \_ Portoghese)            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> <dt>

[**Profili di sistema**](system-profiles.md)
</dt> </dl>

 

 




