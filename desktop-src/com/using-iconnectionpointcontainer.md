---
title: Uso di IConnectionPointContainer
description: Uso di IConnectionPointContainer
ms.assetid: a87afb25-4d45-4ce2-9b27-840da5107bce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d0b7c691e1ba6a8445af56978b43a2ccbf33e7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "106299347"
---
# <a name="using-iconnectionpointcontainer"></a>Uso di IConnectionPointContainer

Un oggetto collegabile implementa [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) (e lo espone tramite [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))) per indicare l'esistenza delle interfacce in uscita. Per ogni interfaccia in uscita, l'oggetto collegabile gestisce un oggetto secondario del punto di connessione, che a sua volta implementa [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint). L'oggetto collegabile contiene quindi i punti di connessione, di conseguenza la denominazione di **IConnectionPointContainer** e **IConnectionPoint**.

Tramite [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer), un client può eseguire due operazioni. Prima di tutto, se il client ha già l'IID per un'interfaccia in uscita supportata, può individuare il punto di connessione corrispondente per l'IID usando [**IConnectionPointContainer:: FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint). Il client non è in grado di eseguire una query per il punto di connessione direttamente a causa della relazione contenitore/contenuto tra l'oggetto collegabile e i punti di connessione contenuti. Fondamentalmente, **FindConnectionPoint** è la [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) per le interfacce in uscita quando l'IID è noto al client.

In secondo luogo, il client può enumerare tutti i punti di connessione all'interno dell'oggetto collegabile tramite [**IConnectionPointContainer:: EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints). Questo metodo restituisce un puntatore a interfaccia [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) per un oggetto enumeratore separato. Tramite [**IEnumConnectionPoints:: Next**](/windows/desktop/api/ocidl/nf-ocidl-ienumconnectionpoints-next), il client può ottenere puntatori di interfaccia [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) a ogni punto di connessione.

Dopo che il client ha ottenuto l'interfaccia [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) , deve chiamare [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) per determinare l'IID dell'interfaccia in uscita supportata da ogni punto di connessione. Se il client supporta già tale interfaccia in uscita, può stabilire una connessione. In caso contrario, può comunque essere in grado di supportare l'interfaccia in uscita usando le informazioni della libreria dei tipi dell'oggetto collegabile per fornire supporto in fase di esecuzione. Questa tecnica richiede che l'oggetto collegabile supporti l'interfaccia [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) . Vedere [uso di IProvideClassInfo](using-iprovideclassinfo.md).

Poiché l'enumeratore è un oggetto separato, il client deve chiamare **IEnumConnectionPoints:: Release** quando l'enumeratore non è più necessario. Inoltre, ogni punto di connessione è un oggetto con un conteggio dei riferimenti separato dall'oggetto che lo contiene. Il client deve quindi chiamare anche IConnectionPoint:: Release per ogni punto di connessione a cui si accede tramite l'enumeratore o tramite [**FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce di oggetti collegabili](connectable-object-interfaces.md)
</dt> </dl>

 

 




