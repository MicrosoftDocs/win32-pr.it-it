---
title: WM/MediaClassSecondaryID
description: L'attributo WM/MediaClassSecondaryID contiene il GUID della classe di supporti secondaria.
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- WM/MediaClassSecondaryID windows Media Format
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a37c0b4314a518132d08454ef2cf7472273795cbb0b50f98d22b800e06cc1b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431645"
---
# <a name="wmmediaclasssecondaryid"></a>WM/MediaClassSecondaryID

**L'attributo WM/MediaClassSecondaryID** contiene il GUID della classe di supporti secondaria.

## <a name="global-constant"></a>Costante globale

g \_ wszWMMediaClassSecondaryID

## <a name="data-type"></a>Tipo di dati

**GUID DEL \_ TIPO \_ WMT**

## <a name="remarks"></a>Commenti

Questo attributo deve essere impostato su uno dei valori nella tabella seguente.



| GUID della classe secondaria                   | Descrizione                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "E0236BEB-C281-4EDE-A36D-7AF76A3D45B5" | Usare per i file di libri audio.                                                                                                                                                               |
| "3A172A13-2BD9-4831-835B-114F6A95943F" | Usare per i file audio che contengono parole parlate, ma non sono libri audio. Ad esempio, routine di stand-up comedy.                                                                           |
| "6677DB9B-E5A0-4063-A1AD-ACEB52840CF1" | Usare per i file audio correlati alle notizie.                                                                                                                                                    |
| "1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B" | Usare per i file audio con contenuto talk show.                                                                                                                                             |
| "1FE2E091-4E1E-40CE-B22D-348C732E0B10" | Usare per i file video correlati alle notizie.                                                                                                                                                    |
| "D6DE1D88-C77C-4593-BFBC-9C61E8C373E3" | Usare per i file video contenenti show basati sul Web, brevi film, trailer di film e così via. Questo è l'identificatore generale per l'intrattenimento video che non rientra in un'altra categoria. |
| "00033368-5009-4AC3-A820-5D2D09A4E7C1" | Usare per i file audio contenenti clip audio dei giochi.                                                                                                                                  |
| "F24FF731-96FC-4D0F-A2F5-5A3483682B1A" | Usare per i file audio contenenti brani completi delle tracce audio del gioco. Se nel file è codificata solo una parte di un brano, usare invece l'identificatore per le clip audio del gioco.                   |
| "E3E689E2-BA8C-4330-96DF-A0EEEFFA6876" | Usare per i file video contenenti video musicali.                                                                                                                                            |
| "B76628F4-300D-443D-9CB5-01C285109DAF" | Usare per i file video contenenti video di home page generali.                                                                                                                                      |
| "A9B87FC9-BD47-4BF0-AC4F-655B89F7D868" | Usare per i file video contenenti film di funzionalità.                                                                                                                                           |
| "BA7F258A-62F7-47A9-B21F-4651C42A000E" | Usare per i file video contenenti programmi televisivi. Per gli show basati sul Web, usare l'identificatore più generico.                                                                                  |
| "44051B5B-B103-4B5C-92AB-93060A9463F0" | Usare per i file video contenenti video aziendali. Ad esempio, riunioni registrate o video di training.                                                                                      |
| "0B710218-8C0C-475E-AF73-4C41C0C8F8CE" | Usare per i file video contenenti video home realizzati con fotografie.                                                                                                                        |



 

Quando si specifica un identificatore di classe secondario, il file deve contenere anche un attributo dell'identificatore di classe primario.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)
</dt> </dl>

 

 




