---
title: Fornire informazioni sulla classe
description: Fornire informazioni sulla classe
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4505a12d4a7f50a605cbd04cae33805db2b19b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116816"
---
# <a name="providing-class-information"></a>Fornire informazioni sulla classe

Spesso è utile per un client di un oggetto esaminare le informazioni sul tipo di oggetto. Dato il CLSID dell'oggetto, un client può individuare la libreria dei tipi dell'oggetto utilizzando le voci del registro di sistema e quindi analizzare la libreria dei tipi per la voce della coclasse nella libreria che corrisponde al CLSID.

Tuttavia, non tutti gli oggetti hanno un CLSID, sebbene sia ancora necessario fornire informazioni sul tipo. Inoltre, è utile per un client disporre di un modo per chiedere semplicemente a un oggetto le informazioni sul tipo, anziché passare attraverso la tedio per estrarre le stesse informazioni dalle voci del registro di sistema. Questa funzionalità è importante quando si gestiscono le interfacce in uscita sugli oggetti collegabili. (Vedere [uso di IProvideClassInfo](using-iprovideclassinfo.md) per altre informazioni su come gli oggetti collegabili forniscono questa funzionalità).

In questi casi, un client può eseguire una query sull'oggetto per [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) o [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2). Se queste interfacce esistono, il client chiama il metodo [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) per ottenere le informazioni sul tipo per l'interfaccia.

Implementando [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) o [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), un oggetto specifica che può fornire informazioni sul tipo per l'intera classe; ovvero ciò che verrebbe descritto nella relativa sezione di coclasse della relativa libreria dei tipi, se presente. [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) restituisce un puntatore **ITypeInfo** corrispondente alle informazioni sulla coclasse dell'oggetto. Tramite questo puntatore **ITypeInfo** , il client può esaminare tutte le definizioni dell'interfaccia in entrata e in uscita dell'oggetto.

L'oggetto può anche fornire [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2). L'interfaccia **IProvideClassInfo2** è una semplice estensione di [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) che consente di recuperare in modo semplice e rapido gli identificatori di interfaccia in uscita di un oggetto per il set di eventi predefinito. **IProvideClassInfo2** deriva da **IProvideClassInfo**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client e server COM](com-clients-and-servers.md)
</dt> </dl>

 

 




