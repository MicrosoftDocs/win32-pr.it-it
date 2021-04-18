---
description: La classe RealTimeStylus consente di interagire con il flusso di dati dalla penna del Tablet PC. Per interagire con il flusso di dati, aggiungere un oggetto RealTimeStylus all'applicazione e aggiungere plug-in all'oggetto RealTimeStylus.
ms.assetid: 4009aeac-d290-4ea5-a6f5-199010acc84d
title: Uso delle API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676752f242aa428b583390d7c3d38c952b4c0edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306693"
---
# <a name="working-with-the-stylusinput-apis"></a>Uso delle API StylusInput

La classe [**RealTimeStylus**](realtimestylus-class.md) consente di interagire con il flusso di dati dalla penna del Tablet PC. Per interagire con il flusso di dati, aggiungere un oggetto **RealTimeStylus** all'applicazione e aggiungere plug-in all'oggetto **RealTimeStylus** .

I plug-in possono modificare i dati associati a pacchetti in aria, stilo inattivo, pacchetti e metodi di notifica stilo. I plug-in possono annullare i pacchetti in aria e i metodi di notifica dei pacchetti. I plug-in possono anche aggiungere dati dell'applicazione al flusso sotto forma di oggetti [CustomStylusData](/previous-versions/ms575208(v=vs.100)) . Nell'elenco seguente sono disponibili le idee per le categorie comuni di plug-in che è possibile utilizzare o creare.

-   Plug-in di filtro: oggetto che consente di rimuovere o annullare selettivamente i dati nel flusso di dati della penna del tablet.
-   Plug-in del modificatore: oggetto che modifica selettivamente i dati nel flusso di dati della penna del tablet.
-   Plug-in Dynamic-renderer: oggetto che Visualizza i dati della penna del tablet in tempo reale poiché è gestito dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) . In seguito, per gli eventi, ad esempio un aggiornamento del modulo, il plug-in di renderer dinamico o un plug-in di raccolta di input penna potrebbe ricreare l'input penna.
-   Plug-in di riconoscimento: oggetto che analizza lo spostamento della penna del tablet per i movimenti, la grafia o altri glifi.
-   Plug-in dell'agente di raccolta input penna: oggetto che dal flusso di dati della penna del Tablet crea e archivia l'input penna.
-   Plug-in wrapper: un plug-in che funge da interfaccia tra l'oggetto [**RealTimeStylus**](realtimestylus-class.md) e un altro plug-in o oggetto come modo per modificare il comportamento dell'oggetto di cui è stato eseguito il wrapping.

È possibile creare plug-in per il renderer dinamico e la raccolta di input penna per eseguire il rendering in diversi contesti, ad esempio in un file, in un flusso o in un dispositivo di visualizzazione. È anche possibile archiviare l'input penna in diversi formati, ad esempio un oggetto [Ink](/previous-versions/aa515768(v=msdn.10)) , un file con Graphics Interchange Format fortificato (gif), un file di formato con input (ISF) con input (input/input) o altri formati.

Con le API StylusInput sono disponibili due plug-in, ovvero la classe [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) e la classe [**GestureRecognizer**](gesturerecognizer-class.md) . La classe **DynamicRenderer** fornisce il rendering di base dei dati di input penna in tempo reale ed è semplificata in modo da avere un effetto minimo sulle prestazioni. La classe **GestureRecognizer** fornisce il riconoscimento dei movimenti per la classe [**RealTimeStylus**](realtimestylus-class.md) .

## <a name="in-this-section"></a>Contenuto della sezione

-   [Uso della classe RealTimeStylus](working-with-the-realtimestylus-class.md)
-   [Plug-in e classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
-   [Dati plug-in e classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
-   [Note sull'implementazione per le API StylusInput](implementation-notes-for-the-stylusinput-apis.md)
-   [Plug-in per la raccolta di input penna](ink-collection-plug-ins.md)
-   [Plug-in di renderer dinamici](dynamic-renderer-plug-ins.md)
-   [Plug-in di riconoscimento](recognizer-plug-ins.md)

 

 
