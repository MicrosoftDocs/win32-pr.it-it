---
title: Opzione di associazione rapida per operazioni di scrittura/modifica batch
description: Quando viene associato un oggetto servizio directory, ADSI crea un oggetto COM che rappresenta l'oggetto directory specificato.
ms.assetid: cf41b0c4-7459-49cf-945b-8462c7d19947
ms.tgt_platform: multiple
keywords:
- Opzione di associazione rapida per operazioni di scrittura/modifica batch ADSI
- ADSI ADSI , uso, opzione di associazione rapida per operazioni di scrittura/modifica batch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f27cbbe9ea76089ca1fd460f76c56d10e60664ae39ad28945440c6006acb9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179900"
---
# <a name="fast-binding-option-for-batch-writemodify-operations"></a>Opzione di associazione rapida per operazioni di scrittura/modifica batch

Quando viene associato un oggetto servizio directory, ADSI crea un oggetto COM che rappresenta l'oggetto directory specificato. Durante l'associazione, ADSI recupera in genere l'attributo **objectClass** in modo che ADSI possa esporre le interfacce COM appropriate per tale classe di oggetto. Ad esempio, un oggetto utente espone [**l'interfaccia IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) oltre alle interfacce ADSI di base supportate per tutti gli oggetti. Per una singola operazione, questa operazione non dovrebbe avere alcun effetto sulle prestazioni. Tuttavia, se vengono eseguite operazioni batch che richiedono centinaia o migliaia di associazioni su una connessione lenta e tali operazioni scrivono dati nel servizio directory, può essere opportuno scambiare il supporto completo degli oggetti per un'associazione più veloce. Questa operazione è nota come associazione rapida e viene eseguita specificando il flag **\_ \_ ADS FAST BIND** quando viene chiamato [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject::OpenDSObject.**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)

L'associazione rapida presenta le restrizioni seguenti:

-   L'operazione di associazione deve essere eseguita con la [**funzione ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o il metodo [**IADsOpenDSObject::OpenDSObject.**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) L'operazione di associazione passa al server di directory una volta anziché due volte. ADSI non recupera **l'attributo objectClass** e pertanto espone solo le interfacce ADSI di base per l'oggetto.
-   Per l'oggetto COM sono supportate le interfacce seguenti:

    -   [**IAD**](/windows/desktop/api/Iads/nn-iads-iads)
    -   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
    -   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
    -   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
    -   [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
    -   [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
    -   [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)
    -   [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)

-   Se il [**metodo IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) viene usato per l'associazione a oggetti figlio, l'oggetto figlio ha le stesse caratteristiche di associazione rapida dell'oggetto padre.
-   L'esistenza dell'oggetto a cui viene associato non viene verificata durante l'operazione di associazione, pertanto le chiamate successive al metodo avranno esito negativo se l'oggetto non esiste. Per questo problema, l'associazione rapida deve essere usata solo per gli oggetti a cui è nota l'esistenza, ad esempio direttamente dopo l'esecuzione di una query che ha restituito i nomi distinti degli oggetti a cui è stata eseguita l'associazione.
-   Le estensioni ADSI vengono esposte per gli oggetti della **classe top**. Di conseguenza, vengono esposte solo le estensioni per le interfacce ADSI di base elencate in precedenza.

 

 