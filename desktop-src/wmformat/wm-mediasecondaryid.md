---
title: WM/MediaClassSecondaryID
description: L'attributo WM/MediaClassSecondaryID contiene il GUID della classe multimediale secondaria.
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- Formato di Windows Media WM/MediaClassSecondaryID
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5923ff0ff0545f1feb769973f2528bd82e351e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397903"
---
# <a name="wmmediaclasssecondaryid"></a>WM/MediaClassSecondaryID

L'attributo **WM/MediaClassSecondaryID** contiene il GUID della classe multimediale secondaria.

## <a name="global-constant"></a>Costante globale

g \_ wszWMMediaClassSecondaryID

## <a name="data-type"></a>Tipo di dati

**\_GUID di tipo WMT \_**

## <a name="remarks"></a>Commenti

Questo attributo deve essere impostato su uno dei valori riportati nella tabella seguente.



| GUID classe secondaria                   | Descrizione                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "E0236BEB-C281-4EDE-A36D-7AF76A3D45B5" | Utilizzare per i file di audiolibro.                                                                                                                                                               |
| "3A172A13-2BD9-4831-835B-114F6A95943F" | Utilizzare per i file audio che contengono parole pronunciate, ma che non sono libri audio. Ad esempio, le routine della commedia di base.                                                                           |
| "6677DB9B-E5A0-4063-A1AD-ACEB52840CF1" | Usare per i file audio correlati alle notizie.                                                                                                                                                    |
| "1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B" | Usare per i file audio con contenuto di talk show.                                                                                                                                             |
| "1FE2E091-4E1E-40CE-B22D-348C732E0B10" | Usare per i file video correlati alle notizie.                                                                                                                                                    |
| "D6DE1D88-C77C-4593-BFBC-9C61E8C373E3" | Da usare per i file video contenenti le esposizioni basate sul Web, i cortometraggi, i trailer di film e così via. Si tratta dell'identificatore generale per gli intrattenimenti video che non rientrano in un'altra categoria. |
| "00033368-5009-4AC3-A820-5D2D09A4E7C1" | Da usare per i file audio contenenti clip audio dei giochi.                                                                                                                                  |
| "F24FF731-96FC-4D0F-A2F5-5A3483682B1A" | Usare per i file audio che contengono brani completi dalle tracce audio del gioco. Se nel file è codificata solo una parte di un brano, usare invece l'identificatore per i clip audio del gioco.                   |
| "E3E689E2-BA8C-4330-96DF-A0EEEFFA6876" | Da usare per i file video contenenti video musicali.                                                                                                                                            |
| "B76628F4-300D-443D-9CB5-01C285109DAF" | Da usare per i file video contenenti il video generale generale.                                                                                                                                      |
| "A9B87FC9-BD47-4BF0-AC4F-655B89F7D868" | Da usare per i file video contenenti film di funzionalità.                                                                                                                                           |
| "BA7F258A-62F7-47A9-B21F-4651C42A000E" | Da usare per i file video contenenti le trasmissioni televisive. Per gli show basati sul Web, usare l'identificatore più generico.                                                                                  |
| "44051B5B-B103-4B5C-92AB-93060A9463F0" | Da usare per i file video contenenti video aziendali. Ad esempio, riunioni registrate o video di formazione.                                                                                      |
| "0B710218-8C0C-475E-AF73-4C41C0C8F8CE" | Da usare per i file video contenenti video privati da fotografie.                                                                                                                        |



 

Quando si specifica un identificatore di classe secondaria, il file deve contenere anche un attributo di identificatore di classe primario.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)
</dt> </dl>

 

 




