---
description: Questo argomento descrive gli identificatori di ordinamento, che possono essere usati nella preparazione degli identificatori delle impostazioni locali.
ms.assetid: abef64b5-ca3f-4cb3-92f0-1b7286bfb686
title: Identificatori di ordinamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a09d8f33285fc5665eff72bbfe1e2075597216
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349786"
---
# <a name="sort-order-identifiers"></a>Identificatori di ordinamento

Questo argomento descrive gli identificatori di ordinamento, che possono essere usati nella preparazione degli [identificatori delle impostazioni locali](locale-identifiers.md). Un identificatore di ordinamento viene definito nel formato " \_ SortOrder", alla fine del nome delle impostazioni locali usato nell'identificatore, ad esempio "de-de \_ phoneb", dove "phoneb" è il tipo di ordinamento. L'identificatore delle impostazioni locali corrispondente viene creato nel modo seguente: `MAKELCID(MAKELANGID(LANG_GERMAN, SUBLANG_GERMAN), SORT_GERMAN_PHONE_BOOK)` .



| Costante                      | Nome delle impostazioni locali                                                                                         | Significato                                                           |
|-------------------------------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Ordina \_ \_ Big5 cinese           | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | Ordine BIG5 cinese                                                |
| Ordina \_ \_ BOPOMOFO cinese       | zh-TW \_ pronun                                                                                       | Ordine Bopomofo cinese tradizionale                                |
| Ordina \_ \_ libro di telefono cinese \_    | zh-CN \_ phoneb<br/>                                                                            | Ordine del libro telefonico cinese (cognome)                                |
| ORDINARE \_ la \_ Repubblica popolare cinese            | tratto zh-CN \_<br/> tratto ZH-HK \_<br/> tratto zh-MO \_<br/> tratto zh-SG \_<br/> | Ordine di conteggio tratti cinese PRC                                    |
| Ordina \_ \_ Prcp cinese           | zh-CN<br/> zh-SG<br/>                                                                   | Ordine fonetico cinese Repubblica popolare cinese                                        |
| Ordina \_ \_ RADICALSTROKE cinese  | zh-TW<br/> zh-HK<br/> zh-MO<br/>                                                  | Ordine radicale/tratto cinese                                      |
| Ordina \_ \_ Unicode cinese        | —                                                                                                   | Ordine Unicode cinese **Windows 2000:** non supportato.<br/>  |
| ORDINAMENTO \_ predefinito                 | Nome delle impostazioni locali uguale al nome della lingua corrispondente                                     | Ordinamento predefinito                                                |
| Ordina \_ georgiano \_ moderno        | KA-GE \_ moderno                                                                                       | Ordine moderno georgiano                                             |
| ORDINAMENTO \_ tradizionale georgiano \_   | ka-GE                                                                                               | Ordine tradizionale georgiano                                        |
| Ordina \_ \_ libro telefonico \_ tedesco     | de-DE \_ phoneb                                                                                       | Ordine del libro telefonico tedesco                                           |
| Ordina \_ \_ valore predefinito ungherese      | hu-HU                                                                                               | Ordine predefinito ungherese                                           |
| ORDINARE \_ le \_ tecniche ungheresi    | HU-HU \_ technl                                                                                       | Ordine tecnico ungherese                                         |
| Ordina \_ \_ RADICALSTROKE giapponese | ja-JP                                                                                               | Ordine radicale/tratto giapponese                                     |
| Ordina \_ \_ Unicode giapponese       | —                                                                                                   | Ordine Unicode giapponese **Windows 2000:** non supportato.<br/> |
| Ordina \_ \_ Xjis giapponese          | ja-JP                                                                                               | Ordine XJIS giapponese                                               |
| ORDINAMENTO \_ coreano \_ KSC             | ko-KR                                                                                               | Ordine del KSC coreano                                                  |
| Ordina \_ \_ Unicode coreano         | —                                                                                                   | Ordine Unicode coreano **Windows 2000:** non supportato.<br/>   |



 

 

 




