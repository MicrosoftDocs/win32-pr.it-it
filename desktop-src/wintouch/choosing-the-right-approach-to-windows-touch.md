---
title: Scelta dell'approccio giusto per Windows Touch
description: In questa sezione vengono illustrati i diversi approcci a Windows Touch che è possibile utilizzare.
ms.assetid: 983023e4-355b-45ba-8572-d93c460d2ff8
keywords:
- Windows Touch, approcci diversi
- Windows Touch, scelta degli approcci
- Windows Touch, miglioramento delle applicazioni
- Windows Touch, supporto zoom
- Windows Touch, supporto legacy
- Plug-in di Windows Touch, RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cdd35b73989541fadd5449efbb3f95d76bfa5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047120"
---
# <a name="choosing-the-right-approach-to-windows-touch"></a>Scelta dell'approccio giusto per Windows Touch

In questa sezione vengono illustrati i diversi approcci a Windows Touch che è possibile utilizzare.

È possibile migliorare le applicazioni utilizzando le funzionalità di Windows Touch in molti modi. Prima di adottare un metodo, è necessario considerare cosa si vuole fare con l'applicazione. Gli scenari seguenti sono tipici di Windows Touch:

-   Si vuole che l'applicazione si comporti come nelle versioni legacy di Windows, ma si vuole che i messaggi di Windows Touch si comportino in modo coerente.
-   Si desidera il supporto della rotazione, della traduzione, della panoramica o dello zoom dell'oggetto personalizzato nell'applicazione.
-   Si vuole che l'applicazione abbia un'interpretazione dettagliata dei movimenti tocco di Windows o per interpretare più ritocchi su un'applicazione ottimizzata in modo specifico per l'input di Windows Touch.
-   Si dispone di un'applicazione che utilizza l'oggetto [**RealTimeStylus**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus) e si desidera ottimizzarla con funzionalità tocco di Windows.

## <a name="you-want-your-application-to-behave-as-it-did-in-legacy-versions-of-windows"></a>Si vuole che l'applicazione si comporti come nelle versioni legacy di Windows

In Windows 7, per impostazione predefinita, le applicazioni generano messaggi che abilitano la funzionalità Windows Touch. Ad esempio, i movimenti Pan attivano \_ \* i messaggi di scorrimento WM. Oltre al supporto di Pan, il \_ gestore di movimenti WM predefinito in Windows 7 supporta il feedback dei limiti, lo zoom e la pressione e il tocco. Il feedback dei limiti viene abilitato anche tramite il supporto legacy. Per ulteriori informazioni sul mapping dei movimenti ai messaggi, vedere [Cenni preliminari sui movimenti tocco di Windows](windows-touch-gestures-overview.md) . Per gli sviluppatori che desiderano solo questa funzionalità di base non è necessario utilizzare direttamente l'API Windows Touch.

> [!Note]  
> I gestori della barra di scorrimento personalizzati devono supportare la richiesta **\_ THUMBPOSITION SM** per i messaggi **WM \_ VSCROLL** e devono supportare la richiesta **SB \_ LINELEFT** e la richiesta **SB \_ LINERIGHT** per i messaggi **WM \_ HSCROLL** .

 

-   La sezione [supporto legacy per la panoramica con barre di scorrimento](legacy-support-for-panning-with-scrollbars.md) illustra come garantire che l'applicazione si comportano come previsto dagli utenti in Windows 7.

## <a name="you-want-custom-object-rotation-translation-panning-or-zoom-support"></a>Si desidera il supporto della rotazione, della traduzione, della panoramica o dello zoom dell'oggetto personalizzato

Se si desidera un supporto limitato per il tocco ma il comportamento predefinito offerto da Windows 7 non è adeguato per l'applicazione, è possibile utilizzare i movimenti per migliorare l'applicazione. Utilizzando i movimenti, è possibile interpretare i comandi di movimento gestendo il messaggio del [**\_ movimento WM**](wm-gesture.md) . Altre informazioni sui movimenti sono disponibili nella sezione [movimenti tocco di Windows](guide-multi-touch-gestures.md). Se l'applicazione necessita del supporto solo per le rotazioni a granularità elevata, il supporto per lo zoom migliorato o la panoramica a dito singolo, i movimenti sono l'approccio migliore per lo sviluppo Windows Touch. Oltre a interpretare il messaggio di movimento, è possibile scegliere di disporre del supporto per il feedback dei limiti. Per ulteriori informazioni sui commenti e suggerimenti sui limiti, vedere la sezione [feedback dei limiti](boundary-feedback.md) di [Windows Touch Programming Reference](windows-touch-programming-reference.md). In Windows 7, il prompt dei comandi e Internet Explorer sfruttano i vantaggi offerti dai suggerimenti e dai movimenti del limite.

-   La sezione [miglioramento dell'esperienza di panning a singolo dito](improving-the-single-finger-panning-experience.md) spiega come personalizzare l'esperienza di panoramica gestendo il messaggio di [**\_ movimento WM**](wm-gesture.md) .

## <a name="you-want-fine-grained-gesture-interpretation-or-custom-handling-of-multiple-touch-points"></a>Si vuole interpretare i movimenti con granularità fine o la gestione personalizzata di più punti di tocco

Per avere un controllo ancora più specifico dei movimenti rispetto a quello offerto dal messaggio di [**\_ movimento WM**](wm-gesture.md) o per interpretare più movimenti su più oggetti, è necessario usare il processore di manipolazione. Il processore di manipolazione essenzialmente è un superset dei movimenti. L'utilizzo del processore di manipolazione richiede l'implementazione di un sink di evento per le manipolazioni a cui si inseriscono dati di tocco non elaborati.

Se si desidera che la fisica degli oggetti semplice oltre a interpretare i movimenti, è necessario utilizzare un processore di inerzia insieme al processore di manipolazione. Il processore di inerzia interagisce con il processore di manipolazione prendendo i valori di velocità dal processore di manipolazione al termine della manipolazione.

Se si vuole interpretare più punti di tocco nell'applicazione, è necessario creare un gestore di messaggi per il messaggio [**WM \_ touch**](wm-touchdown.md) .

-   La sezione [input Windows Touch](guide-multi-touch-input.md) spiega come è possibile interpretare il messaggio [**WM \_ touch**](wm-touchdown.md) .
-   La sezione [rilevamento e rilevamento di più punti di tocco](detecting-and-tracking-multiple-touch-points.md) illustra come creare un'applicazione semplice che interpreta più input.
-   Nella sezione [modifiche e inerzia](manipulation-and-inertia.md) viene illustrato come abilitare l'approccio più flessibile per Windows Touch.

## <a name="you-want-to-enable-windows-touch-input-to-an-application-that-uses-the-realtimestylus"></a>Si vuole abilitare l'input di Windows Touch per un'applicazione che usa RealTimeStylus

Se si desidera abilitare l'input per più contatti sulla piattaforma Tablet PC, è necessario implementare un plug-in di RealTimeStylus personalizzato che interpreta i dati di Windows Touch. Microsoft ha introdotto le interfacce [**ITablet3**](/windows/desktop/tablet/itablet3) e [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3) per abilitare l'input da più contatti nel plug-in RealTimeStylus. Queste interfacce semplificano l'estensione dei plug-in di RealTimeStylus per supportare più punti di contatto.

Per verificare se è abilitato il supporto per più contatti, chiamare la funzionalità di [**multitocco**](/windows/desktop/tablet/itablet3-ismultitouch). Per verificare il numero di contatti supportati, chiamare [**GetMaximumCursors**](/windows/desktop/tablet/itablet3-getmaximumcursors). Per abilitare o disabilitare il supporto di più contatti, chiamare [**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled).

> [!Note]  
> Se non si abilitano più punti di contatto in RealTimeStylus, si riceveranno messaggi di movimento, ad esempio Pan e zoom.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 