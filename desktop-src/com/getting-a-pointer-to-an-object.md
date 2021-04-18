---
title: Recupero di un puntatore a un oggetto
description: Recupero di un puntatore a un oggetto
ms.assetid: 4af9d356-402b-4e69-9f6e-8589057d3ac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0476d36390e7077e7fdd75eef8d95e8173683891
ms.sourcegitcommit: 307b14e9847ced354a52a1ac12d7f659722d99bb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/06/2020
ms.locfileid: "106299491"
---
# <a name="getting-a-pointer-to-an-object"></a>Recupero di un puntatore a un oggetto

Poiché COM non dispone di un modello di classe rigoroso, è possibile creare un'istanza di un client o ottenere un puntatore a un'interfaccia su un oggetto in quattro modi:

-   Chiamare una funzione della libreria COM che crea un oggetto di un tipo predeterminato; ovvero, la funzione restituirà un puntatore a una sola interfaccia specifica per una classe di oggetti specifica.
-   Chiamare una funzione della libreria COM in grado di creare un oggetto basato su un identificatore di classe (CLSID) e che restituisce qualsiasi tipo di puntatore a interfaccia richiesto.
-   Chiamare un metodo di un'interfaccia che crea un altro oggetto (o si connette a un oggetto esistente) e restituisce un puntatore a interfaccia su tale oggetto separato.
-   Implementare un oggetto con un'interfaccia tramite la quale gli altri oggetti passano il puntatore di interfaccia direttamente al client.

Per informazioni su come ottenere i puntatori ad altre interfacce in un oggetto dopo averne il primo, vedere [QueryInterface: navigazione in un oggetto](queryinterface--navigating-in-an-object.md).

## <a name="creating-an-object-of-a-predetermined-type"></a>Creazione di un oggetto di un tipo predeterminato

Sono disponibili numerose funzioni COM, ad esempio [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc), che restituiscono puntatori a implementazioni specifiche dell'interfaccia. (**CoGetMalloc** recupera un puntatore all'allocatore di memoria com standard). La maggior parte di queste funzioni di supporto e la maggior parte di queste funzioni sono descritte nelle sezioni di riferimento di questa documentazione, nell'area specifica a cui sono correlate, ad esempio l'archiviazione o il trasferimento dei dati.

## <a name="creating-an-object-based-on-a-clsid"></a>Creazione di un oggetto basato su un CLSID

Esistono diverse funzioni che, dato un CLSID, un client può chiamare per creare un'istanza dell'oggetto e ottenere un puntatore. Tutte queste funzioni sono basate sulla funzione [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), che crea un oggetto classe e fornisce un puntatore a un'interfaccia che consente di creare istanze di tale classe. Sebbene sia necessario disporre di informazioni sul sistema in cui risiede il server, non è necessario che tali informazioni siano contenute nel client. È necessario che il client conosca solo il CLSID e mai il percorso assoluto del codice server. Per ulteriori informazioni, vedere [creazione di un oggetto tramite un oggetto classe](creating-an-object-through-a-class-object.md).

## <a name="returning-a-pointer-to-a-separate-object"></a>Restituzione di un puntatore a un oggetto separato

Tra i molti metodi di interfaccia che restituiscono un puntatore a un oggetto separato sono diversi che creano e restituiscono un puntatore a un *oggetto enumeratore*, che consente di determinare il numero di elementi di un determinato tipo mantenuto da un oggetto. COM definisce le interfacce per l'enumerazione di un'ampia varietà di elementi, ad esempio stringhe, strutture importanti, moniker e puntatori di interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Il modo più comune per creare un'istanza di enumeratore e ottenere un puntatore alla relativa interfaccia consiste nel chiamare un metodo da un'altra interfaccia. L'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , ad esempio, definisce due metodi, [**EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise) e [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), che restituiscono puntatori a interfacce su due diversi oggetti di enumerazione. Sono disponibili molti altri esempi in COM di metodi che restituiscono puntatori a oggetti, ad esempio l'interfaccia del documento composito OLE [**IOleObject:: GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite), che, quando viene chiamato sull'oggetto incorporato o collegato, restituisce un puntatore all'implementazione dell'oggetto contenitore di [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite).

## <a name="implementing-an-object-through-which-to-pass-an-interface-pointer-directly-to-the-client"></a>Implementazione di un oggetto tramite il quale passare un puntatore di interfaccia direttamente al client

Quando due oggetti, ad esempio un contenitore e un server di documenti compositi OLE, necessitano di comunicazione bidirezionale, ognuno implementa un oggetto contenente un metodo di interfaccia tramite il quale può passare un puntatore di interfaccia all'altro oggetto. L'oggetto di implementazione, che è anche il client dell'oggetto creato, può quindi chiamare il metodo e ottenere il puntatore che è stato passato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client e server COM](com-clients-and-servers.md)
</dt> <dt>

[Responsabilità server COM](com-server-responsibilities.md)
</dt> </dl>

 

 




