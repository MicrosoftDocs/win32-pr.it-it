---
description: Il Tablet PC include la tecnologia per l'interazione con i dati della penna del tablet mentre vengono raccolti.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Accesso e modifica dell'input dello stilo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333126f195154241333127ec585864bd9d592a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305363"
---
# <a name="accessing-and-manipulating-stylus-input"></a>Accesso e modifica dell'input dello stilo

Il Tablet PC include la tecnologia per l'interazione con i dati della penna del tablet mentre vengono raccolti. La classe [**RealTimeStylus**](realtimestylus-class.md) fa parte dell'API (Application Programming Interface) di StylusInput, che fornisce l'accesso al flusso di dati della penna del tablet. Queste API consentono di acquisire, interrompere e modificare il flusso in modo indipendente dal rendering e dalla raccolta di input penna.

Le API StylusInput sono progettate per:

-   Fornire l'accesso in tempo reale al flusso di dati della penna del tablet.
-   Impedire al thread dell'interfaccia utente di bloccare il rendering dinamico degli input penna accodando i dati dei pacchetti nel thread dell'interfaccia utente e creando una raccolta di input penna a thread singolo.
-   Aumentare le prestazioni e ridurre l'utilizzo complessivo dei thread rispetto all'utilizzo dell'oggetto [**InkCollector**](inkcollector-class.md) , dell'oggetto [**InkOverlay**](inkoverlay-class.md) , del controllo [InkPicture](inkpicture-control-reference.md) o del controllo [InkEdit](inkedit-control-reference.md) per raccogliere input penna.

Le API StylusInput non sono progettate per funzionare con l'oggetto [**InkCollector**](inkcollector-class.md) , l'oggetto [**InkOverlay**](inkoverlay-class.md) , il controllo [InkPicture](inkpicture-control-reference.md) o il controllo [InkEdit](inkedit-control-reference.md) .

Quando è necessario interagire direttamente con il flusso di dati della penna del tablet o quando l'applicazione può bloccare l'Inking in tempo reale, usare l'oggetto [**RealTimeStylus**](realtimestylus-class.md) . Utilizzare l'oggetto [**InkCollector**](inkcollector-class.md) , l'oggetto [**InkOverlay**](inkoverlay-class.md) , il controllo [InkPicture](inkpicture-control-reference.md) o il controllo [InkEdit](inkedit-control-reference.md) quando il comportamento predefinito di questi oggetti fornisce il comportamento necessario.

## <a name="in-this-section"></a>Contenuto della sezione

Le sezioni seguenti descrivono gli elementi delle API StylusInput:

-   [Architettura delle API StylusInput](architecture-of-the-stylusinput-apis.md)
-   [Uso delle API StylusInput](working-with-the-stylusinput-apis.md)
    -   [Uso della classe RealTimeStylus](working-with-the-realtimestylus-class.md)
    -   [Plug-in e classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
    -   [Dati plug-in e classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
    -   [Note sull'implementazione per le API StylusInput](implementation-notes-for-the-stylusinput-apis.md)
    -   [Plug-in per la raccolta di input penna](ink-collection-plug-ins.md)
    -   [Plug-in di renderer dinamici](dynamic-renderer-plug-ins.md)
    -   [Plug-in di riconoscimento](recognizer-plug-ins.md)
-   [Considerazioni sull'uso delle API StylusInput](considerations-when-using-the-stylusinput-apis.md)
    -   [Considerazioni di progettazione per le API StylusInput](design-considerations-for-the-stylusinput-apis.md)
    -   [Considerazioni relative al threading per le API StylusInput](threading-considerations-for-the-stylusinput-apis.md)

[Modello di RealTimeStylus a cascata](the-cascaded-realtimestylus-model.md)

-   [Considerazioni sulla gestione degli errori per le API StylusInput](error-handling-considerations-for-the-stylusinput-apis.md)
-   [Considerazioni sulle prestazioni per le API StylusInput](performance-considerations-for-the-stylusinput-apis.md)
-   [Considerazioni sull'attendibilità parziale per le API StylusInput](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di plug-in RealTimeStylus](realtimestylus-plug-in-sample.md)
</dt> <dt>

[Esempio di raccolta inchiostro RealTimeStylus](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



