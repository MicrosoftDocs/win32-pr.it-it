---
description: Le applicazioni Windows dispositivi WIA (Image Acquisition) come albero gerarchico di oggetti IWiaItem o IWiaItem2 con l'elemento radice che rappresenta il dispositivo stesso.
ms.assetid: ae4ded93-09be-4caa-ad6e-1a9071fdb4b6
title: WIA Minidriver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37e8d3c520106c345bd02df5b686bb1abf34f9ff1aa0b338e645b178cabbb874
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056921"
---
# <a name="wia-minidriver"></a>WIA Minidriver

Le applicazioni Windows dispositivi WIA (Image Acquisition) come albero gerarchico di oggetti [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) con l'elemento radice che rappresenta il dispositivo stesso. I dispositivi WIA possono essere usati contemporaneamente da più di un'applicazione. È pertanto necessario che la visualizzazione di ogni applicazione di un oggetto **IWiaItem** o **IWiaItem2** sia indipendente dalle visualizzazioni di un'altra applicazione. Questa operazione viene eseguita con due oggetti elemento diversi. Il driver crea l'albero degli elementi driver degli oggetti [interfaccia IWiaDrvItem,](https://msdn.microsoft.com/library/ms793976.aspx) detti anche elementi driver, usando i metodi dei servizi driver WIA. Si tratta di oggetti globali utilizzati dal driver per rappresentare gli elementi interni di ogni driver. Quando un'applicazione crea un oggetto **IWiaItem** o **IWiaItem2** (detto anche elemento dell'applicazione), questo oggetto viene collegato all'interfaccia [IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) corrispondente del driver nell'albero degli elementi del driver. Un conteggio dei riferimenti viene mantenuto [nell'oggetto interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) in base alle regole seguenti:

-   Quando un driver aggiunge un [oggetto IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) all'albero degli elementi del driver, il conteggio dei riferimenti dell'oggetto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) viene incrementato. Questo avviene in genere durante [IWiaMiniDrv::d rvInitializeWia](https://msdn.microsoft.com/library/ms794097.aspx) o quando viene elaborato un comando \_ SYNCHRONIZE CMD WIA. \_
-   Quando un driver rimuove un oggetto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) dall'albero degli elementi del driver, il conteggio dei riferimenti dell'oggetto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) viene decrementato e l'oggetto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) viene contrassegnato in modo che non possa accedere di nuovo al dispositivo. Questo avviene in genere quando un dispositivo viene disconnesso o viene eliminato un elemento. Le applicazioni sono ancora in grado di leggere le proprietà da un oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) anche quando l'oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) corrispondente è stato rimosso dall'albero degli elementi del driver.
-   Quando viene [**creato, un oggetto IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) viene collegato a un oggetto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) corrispondente. Il conteggio dei riferimenti [dell'oggetto Interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) viene incrementato.
-   Quando viene rilasciato un oggetto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2,**](-wia-iwiaitem2.md) il collegamento all'oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) corrispondente viene danneggiato e il conteggio dei riferimenti dell'oggetto [interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) viene decrementato.
-   Se il conteggio dei riferimenti di un oggetto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) è pari a zero, l'oggetto [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) viene eliminato. Questo vale per tutti gli [oggetti dell'interfaccia IWiaDrvItem,](https://msdn.microsoft.com/library/ms793976.aspx) incluso l'elemento radice. Il conteggio dei riferimenti di un oggetto interfaccia [IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) passa a zero solo quando nessun elemento dell'applicazione vi fa riferimento e non è più collegato all'albero degli elementi del driver.

Usando questo schema di conteggio dei riferimenti, molti oggetti [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) possono essere collegati a [un'interfaccia IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) senza interferenze. Poiché ogni **elemento IWiaItem** o **IWiaItem2** contiene una propria archiviazione delle proprietà, un'applicazione può continuare a leggere le proprietà degli elementi anche dopo l'eliminazione di un elemento, ma nessuna operazione che richiede l'accesso al dispositivo avrà esito positivo. Poiché le proprietà dell'elemento vengono archiviate nell'oggetto **IWiaItem** o **IWiaItem2,** il driver deve impostare le proprietà dell'oggetto **IWiaItem** o **IWiaItem2** sul dispositivo prima di un trasferimento dei dati.

 

 



