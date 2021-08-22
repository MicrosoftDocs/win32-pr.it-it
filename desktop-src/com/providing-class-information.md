---
title: Fornire informazioni sulla classe
description: Fornire informazioni sulla classe
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a042283ca9ba6eb29bceeacef2c32f9bd401ef09e92eafbc737711d0d930336
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500121"
---
# <a name="providing-class-information"></a>Fornire informazioni sulla classe

Spesso è utile per un client di un oggetto esaminare le informazioni sul tipo dell'oggetto. Dato il CLSID dell'oggetto, un client può individuare la libreria dei tipi dell'oggetto usando le voci del Registro di sistema e quindi può analizzare la libreria dei tipi per la voce di coclasse nella libreria corrispondente al CLSID.

Tuttavia, non tutti gli oggetti hanno un CLSID, anche se devono comunque fornire informazioni sul tipo. Inoltre, è utile per un client avere un modo per chiedere semplicemente a un oggetto informazioni sul tipo anziché passare attraverso tutto il tedium per estrarre le stesse informazioni dalle voci del Registro di sistema. Questa funzionalità è importante quando si gestiscono interfacce in uscita su oggetti collegabili. Per altre informazioni sul modo in cui gli oggetti collegabili forniscono questa funzionalità, vedere Uso di [IProvideClassInfo.](using-iprovideclassinfo.md)

In questi casi, un client può eseguire una query sull'oggetto [**per IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) o [**IProvideClassInfo2.**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) Se queste interfacce esistono, il client chiama il [**metodo GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) per ottenere le informazioni sul tipo per l'interfaccia.

Implementando [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) o [**IProvideClassInfo2,**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2)un oggetto specifica che può fornire informazioni sul tipo per l'intera classe. ciò che descrive nella sezione della coclasse della libreria dei tipi, se presente. [**GetClassInfo restituisce**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) un **puntatore ITypeInfo** corrispondente alle informazioni sulla coclasse dell'oggetto. Tramite questo **puntatore ITypeInfo,** il client può esaminare tutte le definizioni di interfaccia in ingresso e in uscita dell'oggetto.

L'oggetto può anche fornire [**IProvideClassInfo2.**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) **L'interfaccia IProvideClassInfo2** è una semplice estensione di [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) che semplifica e veloci il recupero degli identificatori di interfaccia in uscita di un oggetto per il set di eventi predefinito. **IProvideClassInfo2** deriva da **IProvideClassInfo.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client e server COM](com-clients-and-servers.md)
</dt> </dl>

 

 




