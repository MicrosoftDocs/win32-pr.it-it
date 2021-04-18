---
description: Le seguenti considerazioni relative al threading di Tablet PC sono specifiche di quando vengono usati Component Object Model (COM) e l'automazione.
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: Considerazioni sul threading di automazione e COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305694"
---
# <a name="com-and-automation-threading-considerations"></a>Considerazioni sul threading di automazione e COM

Le seguenti considerazioni relative al threading di Tablet PC sono specifiche di quando vengono usati Component Object Model (COM) e l'automazione.

-   [Thread safety](#thread-safety)
-   [Applicazioni STA e MTA](#sta-and-mta-applications)
-   [InkCollector e InkOverlay](#inkcollector-and-inkoverlay)
-   [Sink di evento](#event-sinks)
-   [Eccezioni nei gestori eventi](#exceptions-within-event-handlers)
-   [Argomenti correlati](#related-topics)

## <a name="thread-safety"></a>Thread safety

Ad eccezione dei controlli [InkPicture](inkpicture-control.md) e [InkEdit](inkedit-control.md) , gli oggetti Tablet PC sono thread-safe e sono contrassegnati come entrambi. Essendo contrassegnate come entrambe, possono essere eseguite in un Apartment a thread singolo (STA) o in un Apartment a thread multipli (MTA).

Windows Form usa il modello STA perché Windows Forms è basato su finestre Win32 native che sono intrinsecamente thread-apartment.

## <a name="sta-and-mta-applications"></a>Applicazioni STA e MTA

Se l'applicazione viene eseguita in un MTA o utilizza il gestore di marshalling a thread libero (FTM), è necessario scrivere codice thread-safe; Tuttavia, in questo modo è possibile migliorare determinati problemi di prestazioni di gestione degli eventi.

## <a name="inkcollector-and-inkoverlay"></a>InkCollector e InkOverlay

L'applicazione non deve rilasciare il riferimento finale all'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) , eliminando così l'oggetto direttamente dal thread di input penna. Al contrario, l'applicazione deve rilasciare l'oggetto **InkCollector** o l'oggetto **InkOverlay** da un thread dell'applicazione.

**Attenzione:** Un'applicazione contrassegnata come MTA o utilizza FTM, che consente chiamate dirette dal thread di input penna nell'Apartment dell'applicazione, può rilasciare il riferimento finale all'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) direttamente dal thread di input penna. Tuttavia, ciò causa un errore irreversibile dell'applicazione.

## <a name="event-sinks"></a>Sink di evento

Se l'applicazione non usa il servizio FTM e un oggetto e il relativo sink di evento vengono creati in diversi Apartment, l'evento viene eseguito sul thread che gestisce il sink di evento.

## <a name="exceptions-within-event-handlers"></a>Eccezioni nei gestori eventi

Le eccezioni generate dall'interno dei gestori di eventi di Tablet PC vengono utilizzate e non sono visibili al resto o all'applicazione. Analogamente, i valori HRESULT non vengono propagati dai gestori di eventi Tablet PC. Se un'applicazione che utilizza il livello COM genera un'eccezione, il thread in background termina e l'eccezione andrà persa. Non verranno chiamati gestori di eventi aggiuntivi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di sink di evento C++](c---event-sinks-sample.md)
</dt> <dt>

[Considerazioni generali sul threading](general-threading-considerations.md)
</dt> <dt>

[Considerazioni sul threading della libreria gestita](managed-library-threading-considerations.md)
</dt> </dl>

 

 



