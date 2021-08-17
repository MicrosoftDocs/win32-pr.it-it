---
title: Recupero di un puntatore a un oggetto
description: Recupero di un puntatore a un oggetto
ms.assetid: 4af9d356-402b-4e69-9f6e-8589057d3ac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc588518d5c3da884755d7db122738ca2fca257d76a1f8219867da357ef8444f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736700"
---
# <a name="getting-a-pointer-to-an-object"></a>Recupero di un puntatore a un oggetto

Poiché COM non dispone di un modello di classe strict, un client può creare un'istanza o ottenere un puntatore a un'interfaccia in un oggetto in quattro modi:

-   Chiamare una funzione della libreria COM che crea un oggetto di un tipo predeterminato. in altri, la funzione restituirà un puntatore a una sola interfaccia specifica per una classe di oggetti specifica.
-   Chiamare una funzione della libreria COM che può creare un oggetto basato su un identificatore di classe (CLSID) e che restituisce qualsiasi tipo di puntatore a interfaccia richiesto.
-   Chiamare un metodo di un'interfaccia che crea un altro oggetto (o si connette a uno esistente) e restituisce un puntatore a interfaccia su tale oggetto separato.
-   Implementare un oggetto con un'interfaccia tramite la quale altri oggetti passano direttamente il puntatore a interfaccia al client.

Per informazioni sul recupero di puntatori ad altre interfacce in un oggetto dopo la prima, vedere [QueryInterface: Navigating in an Object](queryinterface--navigating-in-an-object.md).

## <a name="creating-an-object-of-a-predetermined-type"></a>Creazione di un oggetto di un tipo predeterminato

Esistono numerose funzioni COM, ad esempio [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc), che restituiscono puntatori a implementazioni specifiche dell'interfaccia. (**CoGetMalloc** recupera un puntatore all'allocatore di memoria COM standard. La maggior parte di queste sono funzioni helper e la maggior parte di queste funzioni sono descritte nelle sezioni di riferimento di questa documentazione, nell'area specifica a cui sono correlate, ad esempio l'archiviazione o il trasferimento dei dati.

## <a name="creating-an-object-based-on-a-clsid"></a>Creazione di un oggetto basato su un CLSID

Esistono diverse funzioni che, dato un CLSID, un client può chiamare per creare un'istanza dell'oggetto e ottenere un puntatore a esso. Tutte queste funzioni sono basate sulla funzione [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), che crea un oggetto classe e fornisce un puntatore a un'interfaccia che consente di creare istanze di tale classe. Anche se devono essere presenti informazioni che indica il sistema in cui risiede il server, non è necessario che queste informazioni siano contenute nel client. Il client deve conoscere solo il CLSID e mai il percorso assoluto del codice server. Per altre informazioni, vedere [Creazione di un oggetto tramite un oggetto classe](creating-an-object-through-a-class-object.md).

## <a name="returning-a-pointer-to-a-separate-object"></a>Restituzione di un puntatore a un oggetto separato

Tra i molti metodi di interfaccia che restituiscono un puntatore a un oggetto separato sono diversi che creano e restituiscono un puntatore a un oggetto *enumeratore*, che consente di determinare il numero di elementi di un determinato tipo gestito da un oggetto. COM definisce le interfacce per enumerare un'ampia gamma di elementi, ad esempio stringhe, strutture importanti, moniker e puntatori a interfaccia [**IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Il modo tipico per creare un'istanza dell'enumeratore e ottenere un puntatore alla relativa interfaccia è chiamare un metodo da un'altra interfaccia. Ad esempio, [**l'interfaccia IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) definisce due metodi, [**EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise) ed [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), che restituiscono puntatori alle interfacce su due oggetti di enumerazione diversi. Esistono molti altri esempi in COM di metodi che restituiscono puntatori a oggetti, ad esempio l'interfaccia documento composta OLE [**IOleObject::GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite), che, quando viene chiamato sull'oggetto incorporato o collegato, restituisce un puntatore all'implementazione dell'oggetto contenitore [**di IOleClientSite.**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)

## <a name="implementing-an-object-through-which-to-pass-an-interface-pointer-directly-to-the-client"></a>Implementazione di un oggetto tramite il quale passare un puntatore a interfaccia direttamente al client

Quando due oggetti, ad esempio un contenitore di documenti compositi OLE e un server, necessitano di comunicazioni bidirezionali, ognuno implementa un oggetto contenente un metodo di interfaccia tramite il quale può passare un puntatore a interfaccia all'altro oggetto. L'oggetto di implementazione, che è anche il client dell'oggetto creato, può quindi chiamare il metodo e ottenere il puntatore passato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client e server COM](com-clients-and-servers.md)
</dt> <dt>

[Responsabilità del server COM](com-server-responsibilities.md)
</dt> </dl>

 

 




