---
description: Panoramica dell'uso dei movimenti.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Uso di movimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c267cff446d1bb6d092ba50bde21c1b3e25184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966651"
---
# <a name="using-gestures"></a>Uso di movimenti

La piattaforma Tablet PC fornisce il riconoscitore di movimento Microsoft per supportare i movimenti dell'applicazione. Per un elenco dei movimenti supportati dal riconoscitore di movimento Microsoft, vedere la tabella dei movimenti dell'applicazione nell'enumerazione [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) . Il Tablet PC supporta inoltre i movimenti di sistema. Per un elenco dei movimenti del sistema supportati dal Tablet PC, vedere la tabella dei movimenti di sistema nell'enumerazione [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .

## <a name="microsoft-gesture-recognizer"></a>Riconoscimento movimento Microsoft

È possibile utilizzare il riconoscitore di movimento Microsoft utilizzando la proprietà [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) dell'oggetto [**InkCollector**](inkcollector-class.md) , l'oggetto [**InkOverlay**](inkoverlay-class.md) o il controllo [InkPicture](inkpicture-control-reference.md) . Se si imposta la proprietà **CollectionMode** su modalità mista (**InkAndGesture**) o la modalità solo movimento (**GestureOnly**), per impostazione predefinita viene passato l'input penna al riconoscimento di movimento Microsoft. È possibile usare il riconoscitore di movimento Microsoft con il controllo [InkEdit](inkedit-control-reference.md) impostando la proprietà [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) su **InkAndGesture**. È anche possibile usare il riconoscimento dei movimenti con l'oggetto [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) aggiungendo un oggetto [**GestureRecognizer**](gesturerecognizer-class.md) a una delle relative raccolte di plug-in.

Tuttavia, se i movimenti che si vuole usare non sono supportati dalla versione corrente del riconoscitore di movimento Microsoft, è possibile creare il proprio sistema di riconoscimento e usarlo in combinazione con il riconoscitore di movimento Microsoft. Questo consente il supporto completo per i movimenti nell'applicazione.

Il Tablet PC usa una penna per alcuni o tutti gli input. Questo rende estremamente semplice scrivere input penna. La piattaforma Tablet PC fornisce l'architettura per input penna che supporta una struttura a più livelli dei movimenti. I movimenti e il mapping vengono definiti per consentire all'utente di scrivere e richiamare movimenti avanzati su nuove superfici, riservando al tempo stesso i movimenti che richiamano i tradizionali messaggi del mouse di altre applicazioni basate su Windows.

La piattaforma Tablet PC introduce due livelli di movimenti: i movimenti di sistema, noti anche come eventi di sistema e i movimenti dell'applicazione. L'architettura Pen supporta i movimenti del sistema e dell'applicazione. Sono supportati sia i movimenti di applicazione a tratto singolo che quelli a più tratti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Movimenti dell'applicazione](application-gestures.md)
</dt> <dt>

[Movimenti rapidi](flicks-gestures.md)
</dt> <dt>

[Movimenti di sistema](system-gestures.md)
</dt> </dl>

 

 



