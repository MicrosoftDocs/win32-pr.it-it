---
title: Opzione di associazione rapida per le operazioni di scrittura/modifica batch
description: Quando un oggetto servizio directory è associato a, ADSI crea un oggetto COM che rappresenta l'oggetto directory specificato.
ms.assetid: cf41b0c4-7459-49cf-945b-8462c7d19947
ms.tgt_platform: multiple
keywords:
- Opzione di associazione rapida per le operazioni di scrittura/modifica batch ADSI
- ADSI ADSI, uso, opzione di associazione rapida per le operazioni di scrittura/modifica batch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322cf3c8b5f40dc43304f95d08ff53a7c5c14217
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517115"
---
# <a name="fast-binding-option-for-batch-writemodify-operations"></a>Opzione di associazione rapida per le operazioni di scrittura/modifica batch

Quando un oggetto servizio directory è associato a, ADSI crea un oggetto COM che rappresenta l'oggetto directory specificato. Quando si esegue l'associazione, ADSI recupera in genere l'attributo **objectClass** in modo che ADSI possa esporre le interfacce com appropriate per la classe dell'oggetto. Un oggetto utente, ad esempio, esporrà l'interfaccia [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) oltre alle interfacce ADSI di base supportate per tutti gli oggetti. Per una singola operazione, questo non dovrebbe avere alcun effetto sulle prestazioni. Tuttavia, se vengono eseguite operazioni batch che richiedono centinaia o migliaia di binding su una connessione lenta e tali operazioni scrivono dati nel servizio directory, potrebbe essere auspicabile scambiare il supporto completo degli oggetti per un binding più rapido. Questa operazione è nota come associazione veloce e viene eseguita specificando il flag **di \_ \_ associazione rapida ADS** quando viene chiamato [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .

L'associazione rapida presenta le restrizioni seguenti:

-   L'operazione di associazione deve essere eseguita con la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) . L'operazione di associazione viene inviata al server di directory una volta anziché due volte. ADSI non recupera l'attributo **objectClass** ed espone pertanto solo le interfacce ADSI di base per l'oggetto.
-   Per l'oggetto COM sono supportate le interfacce seguenti:

    -   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
    -   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
    -   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
    -   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
    -   [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
    -   [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
    -   [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)
    -   [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)

-   Se il metodo [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) viene usato per l'associazione agli oggetti figlio, l'oggetto figlio ha le stesse caratteristiche di associazione rapida dell'elemento padre.
-   L'esistenza dell'oggetto associato a non viene verificata durante l'operazione di associazione, quindi le chiamate al metodo successive avranno esito negativo se l'oggetto non esiste. Per questo motivo, l'associazione rapida deve essere utilizzata solo per gli oggetti che sono noti, ad esempio, direttamente dopo l'esecuzione di una query che restituisce i nomi distinti degli oggetti a cui viene associato.
-   Le estensioni ADSI sono esposte per gli oggetti della classe **Top**. Vengono pertanto esposte solo le estensioni per le interfacce ADSI di base elencate in precedenza.

 

 