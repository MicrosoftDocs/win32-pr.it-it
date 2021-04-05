---
description: La classe CMediaControl fornisce la gestione delle classi di base dei metodi IDispatch dei IMediaControl a doppia interfaccia. Lascia come virtuale pura le proprietà e i metodi dell'interfaccia IMediaControl.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: Classe CMediaControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae3a528263af4bd2fe5e4eccbe28793799c373a0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886025"
---
# <a name="cmediacontrol-class"></a>Classe CMediaControl

![gerarchia di classi cmediacontrol](images/cutil02.png)

La `CMediaControl` classe fornisce la gestione delle classi di base dei metodi [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) dei [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)a doppia interfaccia. Lascia come virtuale pura le proprietà e i metodi dell'interfaccia **IMediaControl** .

In genere, Filter Graph Manager è l'unico oggetto che implementa l'interfaccia [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) . i filtri implementano l'interfaccia [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) , ereditata da [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), per ricevere i comandi di controllo da gestione grafico dei filtri. Questa libreria di classi è pertanto di uso limitato per filtrare gli sviluppatori.

Le funzioni membro [**CMediaControl:: GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl:: GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl:: GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)e [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) sono implementazioni standard dei metodi [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) che usano la classe [**CBaseDispatch**](cbasedispatch.md) (e una libreria dei tipi) per analizzare i comandi e passarli ai metodi virtuali puri dell'interfaccia [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .

I metodi [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) , definiti in Control. FAD, vengono lasciati come virtuali puri.



| Funzioni di membro                                           | Descrizione                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaControl**](cmediacontrol-cmediacontrol.md)       | Costruisce un oggetto **CMediaControl** .                                                                                                                                                                                                  |
| IDispatch (metodi)                                          | Descrizione                                                                                                                                                                                                                             |
| [**GetIDsOfNames**](cmediacontrol-getidsofnames.md)       | Esegue il mapping di un singolo membro e di un set facoltativo di parametri a un set corrispondente di identificatori di invio di numeri interi (DISPID), che possono essere usati durante le chiamate successive al metodo [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) . |
| [**GetTypeInfo**](cmediacontrol-gettypeinfo.md)           | Recupera un oggetto informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia.                                                                                                                                          |
| [**GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md) | Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto.                                                                                                                                                              |
| [**Richiamare**](cmediacontrol-invoke.md)                     | Fornisce l'accesso a proprietà e metodi esposti da un oggetto.                                                                                                                                                                         |



 

 

 
