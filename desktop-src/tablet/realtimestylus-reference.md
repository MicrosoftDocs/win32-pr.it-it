---
description: Consente di accedere agli eventi dello stilo provenienti dai digitalizzatori penna o touch.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: Riferimento a RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232477"
---
# <a name="realtimestylus-reference"></a>Riferimento a RealTimeStylus

Consente di accedere agli eventi dello stilo provenienti dai digitalizzatori penna o touch.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Classi e interfacce RealTimeStylus](realtimestylus-classes-and-interfaces.md)
-   [Enumerazioni RealTimeStylus](realtimestylus-enumerations.md)
-   [Strutture RealTimeStylus](realtimestylus-structures.md)

## <a name="remarks"></a>Commenti

Questo oggetto implementa l'interfaccia com [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) .

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.

È possibile controllare completamente, eseguire dinamicamente il rendering, modificare e persino eliminare dati dal flusso di pacchetti all'interno dei plug-in sincroni e asincroni dell'oggetto [**classe RealTimeStylus**](realtimestylus-class.md) .

Lo stilo in tempo reale fornisce un modo per creare un oggetto **InkCollecting** a thread singolo e residente nel thread dell'interfaccia utente dell'applicazione. Questo oggetto **InkCollecting** accede ai dati dello stilo in tempo reale dalla coda. Un oggetto **InkCollecting** insieme a stilo in tempo reale consente la modifica in tempo reale della selezione e la modifica in tempo reale dei dati Ink raccolti. Per ulteriori informazioni, vedere [accesso e modifica dell'input dello stilo](accessing-and-manipulating-stylus-input.md).

Usare l'oggetto [**classe RealTimeStylus**](realtimestylus-class.md) per interagire direttamente con il flusso di dati dello stilo del tablet o per bloccare l'Inking in tempo reale. Utilizzare l'oggetto [**classe InkCollector**](inkcollector-class.md) , l'oggetto [**classe InkOverlay**](inkoverlay-class.md) , il controllo di [controllo InkPicture](inkpicture-control-reference.md) o il controllo [InkEdit](inkedit-control-reference.md) quando il comportamento predefinito di questi oggetti fornisce il comportamento necessario.

Gli eventi dello stilo in tempo reale si trovano in un handle di finestra specifico all'interno di un rettangolo di input della finestra specifico. RealTimeStylusService può inviare dati dello stilo a più oggetti [**classe RealTimeStylus**](realtimestylus-class.md) . Ogni oggetto **classe RealTimeStylus** riceve i dati dello stilo per una sezione specifica di una finestra basata sulla [**Proprietà IRealTimeStylus:: WindowInputRectangle**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) definita per l'oggetto **classe RealTimeStylus** . L'oggetto **classe RealTimeStylus** ottiene i dati dello stilo e quindi li elabora tramite un elenco di plug-in sincroni e asincroni.

La differenza tra i plug-in sincroni e i plug-in asincroni risiede nel thread in cui vengono eseguiti e nella sequenza chiamante. I plug-in sincroni vengono chiamati dal thread in cui viene eseguito l'oggetto [**RealTimeStylus Class**](realtimestylus-class.md) . Ogni volta che viene creata un'istanza dell'oggetto **classe RealTimeStylus** , viene creata un'istanza di un thread di esecuzione. I plug-in sincroni vengono eseguiti sul nuovo thread di cui è stata creata un'istanza per l'istanza dell'oggetto **classe RealTimeStylus** . I plug-in asincroni vengono chiamati tramite l'interfaccia utente o il thread dell'applicazione dopo che il flusso di pacchetti è stato elaborato dai plug-in sincroni e archiviato nella coda di output.

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

 

 
