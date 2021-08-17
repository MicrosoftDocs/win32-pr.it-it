---
description: Fornisce l'accesso agli eventi dello stilo provenienti da digitalizzatori a penna o tocco.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: Informazioni di riferimento su RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05518658a7bca01090e72cbe68d23b98d5ffffed14b2d8d091fa8c884e9f7c0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091461"
---
# <a name="realtimestylus-reference"></a>Informazioni di riferimento su RealTimeStylus

Fornisce l'accesso agli eventi dello stilo provenienti da digitalizzatori a penna o tocco.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Classi e interfacce RealTimeStylus](realtimestylus-classes-and-interfaces.md)
-   [Enumerazioni RealTimeStylus](realtimestylus-enumerations.md)
-   [Strutture RealTimeStylus](realtimestylus-structures.md)

## <a name="remarks"></a>Commenti

Questo oggetto implementa [**l'interfaccia COM IRealTimeStylus.**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)

È possibile creare un'istanza di questo oggetto chiamando il [**metodo CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

È possibile controllare, eseguire in modo dinamico il rendering, modificare ed eliminare i dati dal flusso di pacchetti all'interno dei plug-in sincroni e asincroni dell'oggetto [**Classe RealTimeStylus.**](realtimestylus-class.md)

Lo stilo in tempo reale consente di creare un **oggetto InkCollecting** a thread singolo e residente nel thread dell'interfaccia utente dell'applicazione. Questo **oggetto InkCollecting** accede ai dati dello stilo in tempo reale dalla coda. Un **oggetto InkCollecting** in combinazione con lo stilo in tempo reale consente la modifica della selezione in tempo reale e la modifica in tempo reale dei dati dell'input penna raccolti. Per altre informazioni, vedere Accesso e modifica [dell'input dello stilo](accessing-and-manipulating-stylus-input.md).

Usare [**l'oggetto Classe RealTimeStylus**](realtimestylus-class.md) per interagire direttamente con il flusso di dati dello stilo del tablet o per bloccare l'input penna in tempo reale. Usare [**l'oggetto Classe InkCollector,**](inkcollector-class.md) l'oggetto [**Classe InkOverlay,**](inkoverlay-class.md) il controllo [Controllo InkPicture](inkpicture-control-reference.md) o il controllo [InkEdit](inkedit-control-reference.md) quando il comportamento predefinito di questi oggetti fornisce il comportamento necessario.

Gli eventi dello stilo in tempo reale si verificano su un handle di finestra specifico all'interno di un rettangolo di input della finestra specifico. RealTimeStylusService può inviare dati dello stilo a più oggetti della classe [**RealTimeStylus.**](realtimestylus-class.md) Ogni **oggetto Classe RealTimeStylus** riceve i dati dello stilo per una sezione specifica di una finestra in base alla proprietà [**IRealTimeStylus::WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) definita per tale oggetto **Classe RealTimeStylus.** **L'oggetto Classe RealTimeStylus** ottiene i dati dello stilo e quindi li elabora tramite un elenco di plug-in sincroni e asincroni.

La differenza tra i plug-in sincroni e i plug-in asincroni risiede nel thread in cui vengono eseguiti e nella sequenza chiamante. I plug-in sincroni vengono chiamati dal thread in cui viene eseguito l'oggetto [**Classe RealTimeStylus.**](realtimestylus-class.md) Ogni volta **che viene creata un'istanza dell'oggetto Classe RealTimeStylus,** viene creata un'istanza di un thread di esecuzione. I plug-in sincroni vengono eseguiti in questo nuovo thread di cui viene creata un'istanza per l'istanza dell'oggetto **Classe RealTimeStylus.** I plug-in asincroni vengono chiamati tramite l'interfaccia utente o il thread dell'applicazione dopo che il flusso di pacchetti è stato elaborato dai plug-in sincroni e archiviato nella coda di output.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IDynamicRenderer**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
