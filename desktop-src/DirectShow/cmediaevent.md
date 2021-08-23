---
description: La classe CMediaEvent fornisce l'implementazione della classe di base dei metodi IDispatch dell'interfaccia duale IMediaEvent. Lascia come virtuali pure le proprietà e i metodi dell'interfaccia IMediaEvent.
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
ms.openlocfilehash: 505a11b9a8d3c12586e25faa822b127e0b8bb636f6655eb617125a47fb84feaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832486"
---
# <a name="cmediaevent-class"></a>Classe CMediaEvent

![Gerarchia di classi cmediaevent](images/cutil03.png)

La `CMediaEvent` classe fornisce l'implementazione della classe di base **dei metodi IDispatch** dell'interfaccia duale [**IMediaEvent.**](/windows/desktop/api/Control/nn-control-imediaevent) Lascia come virtuali pure le proprietà e i metodi **dell'interfaccia IMediaEvent.**

La `CMediaEvent` classe fornisce anche l'implementazione della classe di base [**dell'interfaccia IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) che deriva da [**IMediaEvent.**](/windows/desktop/api/Control/nn-control-imediaevent)

Le funzioni membro [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent::GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)e [**CMediaEvent::Invoke**](cmediaevent-invoke.md) sono implementazioni standard dell'interfaccia **IDispatch** che usano la classe [**CBaseDispatch**](cbasedispatch.md) (e una libreria dei tipi) per analizzare i comandi e passarli ai metodi virtuali puri dell'interfaccia [**IMediaEvent.**](/windows/desktop/api/Control/nn-control-imediaevent)



| Funzioni di membro                                         | Descrizione                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaEvent**](cmediaevent-cmediaevent.md)           | Costruisce un **oggetto CMediaEvent.**                                                                                                                                                          |
| Metodi IDispatch                                        | Descrizione                                                                                                                                                                                   |
| [**Getidsofnames**](cmediaevent-getidsofnames.md)       | Mappe un singolo membro e un set facoltativo di parametri a un set corrispondente di identificatori di invio integer, che possono essere usati durante le chiamate successive al **metodo IDispatch::Invoke.** |
| [**GetTypeInfo**](cmediaevent-gettypeinfo.md)           | Recupera un oggetto informazioni sul tipo, che recupera le informazioni sul tipo per un'interfaccia.                                                                                                   |
| [**GetTypeInfoCount**](cmediaevent-gettypeinfocount.md) | Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto .                                                                                                                    |
| [**evocare**](cmediaevent-invoke.md)                     | Fornisce l'accesso a proprietà e metodi esposti da un oggetto.                                                                                                                               |



 

 

 



