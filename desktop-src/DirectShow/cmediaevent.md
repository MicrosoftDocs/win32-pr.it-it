---
description: La classe CMediaEvent fornisce l'implementazione della classe di base dei metodi IDispatch dei IMediaEvent a doppia interfaccia. Lascia come virtuale pura le proprietà e i metodi dell'interfaccia IMediaEvent.
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: Classe CMediaEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 927e561fa557ac33b1669ca7353377f7814ca448
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234528"
---
# <a name="cmediaevent-class"></a>Classe CMediaEvent

![gerarchia di classi cmediaevent](images/cutil03.png)

La `CMediaEvent` classe fornisce l'implementazione della classe di base dei metodi **IDispatch** dei [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)a doppia interfaccia. Lascia come virtuale pura le proprietà e i metodi dell'interfaccia **IMediaEvent** .

La `CMediaEvent` classe fornisce anche l'implementazione della classe di base dell'interfaccia [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) che deriva da [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).

Le funzioni membro [**CMediaEvent:: GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent:: GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent:: GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)e [**CMediaEvent:: Invoke**](cmediaevent-invoke.md) sono implementazioni standard dell'interfaccia **IDispatch** usando la classe [**CBaseDispatch**](cbasedispatch.md) (e una libreria dei tipi) per analizzare i comandi e passarli ai metodi virtuali puri dell'interfaccia [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .



| Funzioni di membro                                         | Descrizione                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaEvent**](cmediaevent-cmediaevent.md)           | Costruisce un oggetto **CMediaEvent** .                                                                                                                                                          |
| IDispatch (metodi)                                        | Descrizione                                                                                                                                                                                   |
| [**GetIDsOfNames**](cmediaevent-getidsofnames.md)       | Esegue il mapping di un singolo membro e di un set facoltativo di parametri a un set corrispondente di identificatori di invio di numeri interi, che possono essere usati durante le chiamate successive al metodo **IDispatch:: Invoke** . |
| [**GetTypeInfo**](cmediaevent-gettypeinfo.md)           | Recupera un oggetto informazioni sul tipo, che recupera le informazioni sul tipo per un'interfaccia.                                                                                                   |
| [**GetTypeInfoCount**](cmediaevent-gettypeinfocount.md) | Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto.                                                                                                                    |
| [**Richiamare**](cmediaevent-invoke.md)                     | Fornisce l'accesso a proprietà e metodi esposti da un oggetto.                                                                                                                               |



 

 

 



