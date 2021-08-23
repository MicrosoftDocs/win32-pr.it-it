---
description: La classe CMediaControl fornisce la gestione della classe di base dei metodi IDispatch dell'interfaccia duale IMediaControl. Lascia virtuali come pure le proprietà e i metodi dell'interfaccia IMediaControl.
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
ms.openlocfilehash: 119ffb93cb307db1da3bc8c7562851d63c5f9eeb8e0e3b80be62c8110181c32b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074080"
---
# <a name="cmediacontrol-class"></a>Classe CMediaControl

![Gerarchia di classi cmediacontrol](images/cutil02.png)

La `CMediaControl` classe fornisce la gestione della classe di base dei metodi [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) dell'interfaccia [**duale IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol). Lascia virtuali come pure le proprietà e i metodi **dell'interfaccia IMediaControl.**

In genere, il gestore del grafico filtri è l'unico oggetto che implementa [**l'interfaccia IMediaControl.**](/windows/desktop/api/Control/nn-control-imediacontrol) I filtri implementano [**l'interfaccia IMediaFilter,**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) ereditata da [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)per ricevere i comandi di controllo dal gestore del grafico filtri. Pertanto, questa libreria di classi è di uso limitato per filtrare gli sviluppatori.

Le funzioni membro [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl::GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)e [**CMediaControl::Invoke**](cmediacontrol-invoke.md) sono implementazioni standard dei metodi [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) che usano la classe [**CBaseDispatch**](cbasedispatch.md) (e una libreria dei tipi) per analizzare i comandi e passarli ai metodi virtuali puri dell'interfaccia [**IMediaControl.**](/windows/desktop/api/Control/nn-control-imediacontrol)

I [**metodi IMediaControl,**](/windows/desktop/api/Control/nn-control-imediacontrol) definiti in control.odl, vengono lasciati come virtuali puri.



| Funzioni di membro                                           | Descrizione                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaControl**](cmediacontrol-cmediacontrol.md)       | Costruisce un **oggetto CMediaControl.**                                                                                                                                                                                                  |
| Metodi IDispatch                                          | Descrizione                                                                                                                                                                                                                             |
| [**Getidsofnames**](cmediacontrol-getidsofnames.md)       | Mappe un singolo membro e un set facoltativo di parametri a un set corrispondente di IDENTIFICATORI DISP (Integer Dispatch Identifier), che possono essere usati durante le chiamate successive al metodo [**CMediaControl::Invoke.**](cmediacontrol-invoke.md) |
| [**GetTypeInfo**](cmediacontrol-gettypeinfo.md)           | Recupera un oggetto informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia.                                                                                                                                          |
| [**GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md) | Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto .                                                                                                                                                              |
| [**evocare**](cmediacontrol-invoke.md)                     | Fornisce l'accesso a proprietà e metodi esposti da un oggetto.                                                                                                                                                                         |



 

 

 
