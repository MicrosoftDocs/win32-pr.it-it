---
title: Riferimento al mixer audio
description: Riferimento al mixer audio
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- audio multimediale, mixer audio
- audio, mixer audio
- audio multimediale, riferimento al mixer
- audio, riferimento al mixer
- mixer audio, informazioni di riferimento
- mixer, riferimento
- informazioni di riferimento per i mixer audio, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1d86f305714d72631b56495753417699b1a146
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223857"
---
# <a name="audio-mixer-reference"></a>Riferimento al mixer audio

In questa sezione vengono descritte le funzioni, le strutture e i messaggi associati a mixer audio. Questi elementi vengono raggruppati come indicato di seguito.

## <a name="querying-devices"></a>Esecuzione di query sui dispositivi

-   [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a>Apertura e chiusura

-   [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a>Recupero degli identificatori del mixer

-   [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a>Recupero di controlli linea

-   [**MIXERCONTROL**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a>Modifica degli attributi del controllo

-   [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   [**MIXERCONTROLDETAILS ( \_ booleano)**](/previous-versions//dd757295(v=vs.85))
-   [**\_LISTTEXT MIXERCONTROLDETAILS**](/previous-versions//dd757296(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ firmato**](/previous-versions//dd757297(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ senza segno**](/previous-versions//dd757298(v=vs.85))
-   [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a>Recupero delle informazioni sulla riga

-   [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [**\_ \_ modifica controllo MIXM \_ mm**](mm-mixm-control-change.md)
-   [**\_ \_ modifica riga MIXM \_ mm**](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a>Invio di messaggi di User-Defined

-   [**mixerMessage**](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al mixer audio](audio-mixer-reference.md)
</dt> </dl>

 

 