---
description: Panoramica dell'uso dei movimenti.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Uso dei movimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c4748dbf2638a57e005562fdec735ea6e87c27757d46549b7577f3bed7741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449249"
---
# <a name="using-gestures"></a>Uso dei movimenti

La piattaforma Tablet PC fornisce il riconoscimento dei movimenti Microsoft per supportare i movimenti dell'applicazione. Per un elenco dei movimenti supportati dal sistema di riconoscimento dei movimenti Microsoft, vedere la tabella dei movimenti dell'applicazione [**nell'enumerazione ApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) Il Tablet PC supporta anche i movimenti di sistema. Per un elenco dei movimenti di sistema supportati dal Tablet PC, vedere la tabella dei movimenti di sistema [**nell'enumerazione SystemGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)

## <a name="microsoft-gesture-recognizer"></a>Riconoscimento movimenti Microsoft

È possibile usare il riconoscimento dei movimenti Microsoft usando la [**proprietà CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) dell'oggetto [**InkCollector,**](inkcollector-class.md) [**dell'oggetto InkOverlay**](inkoverlay-class.md) o del [controllo InkPicture.](inkpicture-control-reference.md) L'impostazione della proprietà **CollectionMode** sulla modalità mista (**InkAndGesture**) o solo movimento (**GestureOnly**) passa l'input penna al sistema di riconoscimento dei movimenti Microsoft per impostazione predefinita. È possibile usare il riconoscimento dei movimenti Microsoft con il [controllo InkEdit](inkedit-control-reference.md) impostando la [**proprietà InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) su **InkAndGesture**. È anche possibile usare il riconoscimento dei movimenti con l'oggetto [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) aggiungendo un [**oggetto GestureRecognizer**](gesturerecognizer-class.md) a una delle raccolte di plug-in.

Tuttavia, se i movimenti che si vuole usare non sono supportati dalla versione corrente del riconoscimento dei movimenti Microsoft, è possibile creare un sistema di riconoscimento personalizzato e usarlo insieme al sistema di riconoscimento dei movimenti Microsoft. Ciò consente il supporto completo per i movimenti nell'applicazione.

Il Tablet PC usa una penna per alcuni o tutti gli input. In questo modo è estremamente semplice scrivere l'input penna. La piattaforma Tablet PC offre un'architettura per l'input penna che supporta una struttura a livelli di movimenti. I movimenti e il mapping sono definiti per consentire all'utente di scrivere e richiamare movimenti avanzati su nuove superfici, riservando i movimenti che richiamano i messaggi tradizionali del mouse di altre applicazioni basate su Windows.

La piattaforma Tablet PC introduce due livelli di movimenti: movimenti di sistema, noti anche come eventi di sistema, e movimenti dell'applicazione. L'architettura della penna supporta i movimenti di sistema e dell'applicazione. Sono supportati entrambi i movimenti dell'applicazione a tratto singolo e a più tratti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Movimenti dell'applicazione](application-gestures.md)
</dt> <dt>

[Movimenti di scorrimento rapido](flicks-gestures.md)
</dt> <dt>

[Movimenti di sistema](system-gestures.md)
</dt> </dl>

 

 



