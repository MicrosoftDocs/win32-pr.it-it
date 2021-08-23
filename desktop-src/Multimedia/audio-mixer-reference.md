---
title: Informazioni di Mixer audio
description: Informazioni di Mixer audio
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- audio multimediale, mixer audio
- audio, mixer audio
- audio multimediale, informazioni di riferimento sul mixer
- audio, informazioni di riferimento sul mixer
- mixer audio, riferimento
- mixer, riferimento
- informazioni di riferimento sui mixer audio, informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1602a9ac0631a3e81430285c8cd862215a437c72b03b41d87fad6cefa7e41827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786221"
---
# <a name="audio-mixer-reference"></a>Informazioni di Mixer audio

Questa sezione descrive le funzioni, le strutture e i messaggi associati ai mixer audio. Questi elementi sono raggruppati nel modo seguente.

## <a name="querying-devices"></a>Esecuzione di query sui dispositivi

-   [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a>Apertura e chiusura

-   [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [**mixerApri**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a>Recupero Mixer identificatori

-   [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a>Recupero di controlli line

-   [**MIXERCONTROL**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [**CONTROLLO MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a>Modifica degli attributi del controllo

-   [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   [**MIXERCONTROLDETAILS \_ BOOLEANO**](/previous-versions//dd757295(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ FIRMATO**](/previous-versions//dd757297(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ SENZA SEGNO**](/previous-versions//dd757298(v=vs.85))
-   [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a>Recupero delle informazioni sulla riga

-   [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [**MODIFICA DEL CONTROLLO DI MM \_ MIXM \_ \_**](mm-mixm-control-change.md)
-   [**MODIFICA DELLA RIGA DI MM \_ MIXM \_ \_**](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a>Invio User-Defined messaggi

-   [**mixerMessage**](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di Mixer audio](audio-mixer-reference.md)
</dt> </dl>

 

 