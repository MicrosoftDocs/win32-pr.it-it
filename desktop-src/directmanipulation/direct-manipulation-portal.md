---
description: Le API di manipolazione diretta consentono di creare ottime procedure per la panoramica, lo zoom e il trascinamento dell'esperienza utente. A tale scopo, elabora input tocco su un'area o un oggetto, genera trasformazioni di output e applica le trasformazioni agli elementi dell'interfaccia utente.
ms.assetid: 26358bc5-71e9-40f0-9243-9bddd961a0e5
title: Manipolazione diretta
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6db2a50893914dfb25050768f88cb289a1ecf3ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124317"
---
# <a name="direct-manipulation"></a>Manipolazione diretta

Le API di manipolazione diretta consentono di creare ottime procedure per la panoramica, lo zoom e il trascinamento dell'esperienza utente. A tale scopo, elabora input tocco su un'area o un oggetto, genera trasformazioni di output e applica le trasformazioni agli elementi dell'interfaccia utente. È possibile usare la manipolazione diretta per ottimizzare la velocità di risposta e ridurre la latenza tramite l'elaborazione di input fuori thread, l'hit testing di input fuori thread facoltativo e la stima di input/output.

Qualsiasi applicazione che usa la manipolazione diretta per elaborare interazioni touch Visualizza le animazioni di Windows 8 fluide e i comportamenti di feedback di interazione conformi alle [linee guida per le interazioni utente comuni](/windows/uwp/design/input/).

## <a name="developer-audience"></a>Sviluppatori

L'API di manipolazione diretta è destinata agli sviluppatori esperti che conoscono C/C++, hanno una conoscenza approfondita del [Component Object Model (com)](../com/component-object-model--com--portal.md)e hanno familiarità con i concetti di programmazione di Windows.

## <a name="run-time-requirements"></a>Requisiti di runtime

La manipolazione diretta è stata introdotta in Windows 8. È incluso nelle versioni a 32 bit e a 64 bit.

## <a name="why-use-directmanipulation"></a>Perché usare DirectManipulation

### <a name="handles-interactions-in-a-straightforward-and-consistent-manner"></a>Gestisce le interazioni in modo semplice e coerente

La manipolazione diretta funziona predichiarando i comportamenti e le interazioni per un'area o un oggetto. Una pagina Web, ad esempio, è spesso configurata per la panoramica e lo zoom. In fase di esecuzione, l'input viene quindi associato a questa area/oggetto tramite una semplice chiamata API. Da questo punto in poi la manipolazione diretta esegue tutte le operazioni di elaborazione dell'input, applicando vincoli e personalità e generando le trasformazioni di output.

### <a name="build-responsive-touch-applications"></a>Creazione di applicazioni touch reattive

Per ottimizzare la velocità di risposta e ridurre al minimo la latenza, l'elaborazione della manipolazione diretta avviene in un thread indipendente separato dal thread UI. Di conseguenza, le trasformazioni di output possono essere eseguite in parallelo all'attività sul thread dell'interfaccia utente. L'attività del thread dell'interfaccia utente può includere la logica dell'applicazione, il rendering, il layout e qualsiasi altro elemento che utilizza cicli nel processore.

### <a name="implementation-flexibility"></a>Flessibilità di implementazione

Le interfacce incluse con la manipolazione diretta forniscono un supporto completo per la gestione dell'input, il riconoscimento interazione, le notifiche di feedback e gli aggiornamenti dell'interfaccia utente. Le interfacce incorporano anche servizi di sistema, ad esempio [DirectComposition](../directcomp/directcomposition-portal.md).

## <a name="basic-concepts"></a>Concetti fondamentali

L'implementazione della manipolazione diretta più semplice è costituita da un *viewport*, da un *contenuto* e da *interazioni*. Il *viewport* è un'area in grado di ricevere ed elaborare l'input dalle interazioni utente. È anche l'area del contenuto visibile per l'utente finale. Il *contenuto* è l'oggetto effettivo che gli utenti finali possono vedere ed è ciò che si sposta o ridimensiona in risposta all'interazione dell'utente. Le *interazioni* dell'utente principale (note anche come *modifiche*) supportate dalla manipolazione diretta sono la panoramica e lo zoom. Queste interazioni applicano rispettivamente una trasformazione Converti o Ridimensiona al contenuto all'interno del viewport. È possibile configurare più Viewport (ognuno con il proprio contenuto) in un'unica finestra per creare un'interfaccia utente avanzata.

In questa figura viene illustrata un'implementazione di base della manipolazione diretta prima e dopo la panoramica.

![implementazione di base della manipolazione diretta prima e dopo la panoramica.](images/dm-art-1.png)

Durante l'inizializzazione della manipolazione diretta, viene creata un'istanza dell'oggetto **DCompDirectManipulationCompositor** ed è associato alla manipolazione diretta. Questo oggetto è un wrapper per [DirectComposition](../directcomp/directcomposition-portal.md), che è il compositore del sistema. L'oggetto è responsabile dell'applicazione delle trasformazioni di output e della Guida degli aggiornamenti visivi.

Un contatto rappresenta un punto di tocco identificato dalla **PointerId** fornita nel messaggio [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) . Quando viene ricevuto un messaggio **WM \_ POINTERDOWN** , l'applicazione chiama il [**secontatto**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact). L'applicazione invia una notifica diretta a Manipulationabout i contatti che devono essere gestiti e i viewport che devono rispondere a tali contatti. Gli input della tastiera e del mouse hanno valori **PointerId** speciali che possono essere gestiti in modo appropriato dalla manipolazione diretta.

Nel caso di base precedente, quando [**secontact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) viene chiamato, si verificano alcune operazioni:

- Quando l'utente esegue una panoramica, viene inviato un messaggio [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) all'applicazione per notificare che il contatto è stato utilizzato dalla manipolazione diretta.
- Quando l'utente sposta lo spostamento, il viewport genera gli eventi di aggiornamento che vengono usati dal wrapper [DirectComposition](../directcomp/directcomposition-portal.md) per guidare gli aggiornamenti visivi sullo schermo. Per la Panoramica di un utente in un viewport, il contenuto verrà visualizzato in modo graduale sotto il contatto.
- Quando l'utente solleva il contatto, l'utente vede che il contenuto continua a spostarsi mentre passa in un'animazione di inerzia, rallentando gradualmente fino a raggiungere il punto di riposo finale.

## <a name="processing-keyboard-and-mouse-input"></a>Elaborazione dell'input da tastiera e mouse

La manipolazione diretta consente l'invio manuale dei messaggi della tastiera e del mouse dal thread dell'interfaccia utente dell'applicazione tramite l'API [**ProcessInput**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-processinput) in modo che possano essere gestiti in modo appropriato dalla manipolazione diretta.

## <a name="directmanipulation-and-the-hwnd"></a>DirectManipulation e HWND

La manipolazione diretta è associata a un HWND Win32 per ricevere ed elaborare i messaggi di input del puntatore per tale finestra. Poiché la manipolazione diretta calcola i valori di output, esegue le richiamate asincrone agli oggetti COM (Direct Manipulation [Component Object Model)](../com/component-object-model--com--portal.md) implementati nell'applicazione. Questi callback informano l'applicazione sulla trasformazione applicata agli oggetti. La manipolazione diretta viene attivata sull'HWND specificato chiamando [**Activate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-activate).

## <a name="supporting-documentation"></a>Documentazione di supporto

- [Viewport e contenuto](directmanipulation-viewports-and-content.md)
- [Uso di più viewport in DirectManipulation](directmanipulation-multiple-vieports.md)
- [Elaborazione dell'input con DirectManipulation](directmanipulation-processing-input-with-directmanipulation.md)
- [Motore di composizione](directmanipulation-composition-engine.md)
- [Guida di riferimento alla manipolazione diretta](direct-manipulation-reference.md)

- [BUILD 2013: WCL-022: rendere l'app desktop eccezionale grazie a tocco, mouse e penna](https://channel9.msdn.com/Events/Build/2013/4-022)
- [Esempio di elaborazione di input touch con manipolazione diretta](https://github.com/microsoft/Windows-classic-samples/tree/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/TouchInputDirectManipulation)
