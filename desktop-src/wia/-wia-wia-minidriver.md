---
description: Le applicazioni vedono i dispositivi Windows Image Acquisition (WIA) come albero gerarchico di oggetti IWiaItem o IWiaItem2 con l'elemento radice che rappresenta il dispositivo stesso.
ms.assetid: ae4ded93-09be-4caa-ad6e-1a9071fdb4b6
title: Minidriver WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aadaf55cfe2e8102d4e0e02cf9787b9696e327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526412"
---
# <a name="wia-minidriver"></a>Minidriver WIA

Le applicazioni vedono i dispositivi Windows Image Acquisition (WIA) come albero gerarchico di oggetti [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) con l'elemento radice che rappresenta il dispositivo stesso. I dispositivi WIA possono essere utilizzati simultaneamente da più di un'applicazione. È pertanto necessario che la visualizzazione di un oggetto **IWiaItem** o **IWiaItem2** sia indipendente dalle viste di un'altra applicazione. Questa operazione viene eseguita con due oggetti Item diversi. Il driver crea la struttura ad albero degli elementi del driver degli oggetti dell' [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) , detti anche elementi driver, usando i metodi dei servizi del driver WIA. Si tratta di oggetti globali utilizzati dal driver per rappresentare gli elementi interni di ogni driver. Quando un'applicazione crea un oggetto **IWiaItem** o **IWiaItem2** (detto anche elemento applicazione), questo oggetto viene collegato all' [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) corrispondente del driver nell'albero degli elementi del driver. Un conteggio dei riferimenti viene mantenuto nell'oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) soggetto alle regole seguenti:

-   Quando un driver aggiunge un oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) all'albero degli elementi del driver, il conteggio dei riferimenti dell'oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) viene incrementato. Questa operazione viene in genere eseguita durante [IWiaMiniDrv::D rvinitializewia](https://msdn.microsoft.com/library/ms794097.aspx) o quando \_ \_ viene elaborato un comando WIA cmd Synchronize.
-   Quando un driver rimuove un oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) dall'albero degli elementi del driver, il conteggio dei riferimenti dell'oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) viene decrementato e l'oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) viene contrassegnato in modo da non poter accedere di nuovo al dispositivo. Questo problema si verifica in genere quando un dispositivo è disconnesso o viene eliminato un elemento. Le applicazioni sono ancora in grado di leggere le proprietà da un oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) anche quando l'oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) corrispondente è stato rimosso dalla struttura ad albero degli elementi del driver.
-   Quando viene creato un oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) , questo viene collegato a un oggetto di [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) corrispondente. Il conteggio dei riferimenti dell'oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) viene incrementato.
-   Quando viene rilasciato un oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) , il collegamento all'oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) corrispondente viene interrotto e il conteggio dei riferimenti dell'oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) viene decrementato.
-   Se il conteggio dei riferimenti di un oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) va a zero, l'oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) viene eliminato. Si applica a tutti gli oggetti dell' [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) , incluso l'elemento radice. Il conteggio dei riferimenti di un oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) va a zero solo quando nessun elemento dell'applicazione vi fa riferimento e non è più collegato all'albero degli elementi del driver.

Utilizzando questo schema di conteggio dei riferimenti, molti oggetti [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) possono collegarsi a un' [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) senza interferenze. Poiché ogni **IWiaItem** o **IWiaItem2** contiene la propria archiviazione delle proprietà, un'applicazione può continuare a leggere le proprietà degli elementi anche dopo l'eliminazione di un elemento, ma non verrà eseguita alcuna operazione che richiede l'accesso al dispositivo. Poiché le proprietà degli elementi vengono archiviate nell'oggetto **IWiaItem** o **IWiaItem2** , il driver deve impostare le proprietà dell'oggetto **IWiaItem** o **IWiaItem2** sul dispositivo prima del trasferimento dei dati.

 

 



