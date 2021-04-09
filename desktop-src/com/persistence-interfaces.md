---
title: Interfacce di persistenza
description: Interfacce di persistenza
ms.assetid: a93582b3-bdbf-430d-b4a6-c0df7bc35dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72ef5f7381c6d58b9025f983ecd852b83661030
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118562"
---
# <a name="persistence-interfaces"></a>Interfacce di persistenza

Gli oggetti che hanno uno stato permanente di qualsiasi tipo devono implementare almeno un' \* interfaccia IPersist e preferibilmente più interfacce, per fornire al contenitore la scelta più flessibile di come si desidera salvare lo stato di un controllo.

Se un controllo ha uno stato persistente, deve come minimo implementare [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) (i due si escludono a vicenda e non devono essere implementati insieme per la maggior parte). Quest'ultimo viene usato quando un controllo vuole capire quando viene creato nuovo, anziché ricaricato da uno stato persistente esistente (**IPersistStream** non ha la nuova funzionalità creata). L'esistenza di una delle due interfacce indica che il controllo può salvare e caricare lo stato persistente in un flusso, ovvero un'istanza di [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).

Oltre a queste due interfacce basate su flusso, \* è possibile fornire facoltativamente le interfacce IPersist elencate nella tabella seguente per supportare la persistenza in percorsi diversi da un [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)espandibile.

Un set di categorie di componenti viene identificato per coprire il supporto per le interfacce persistenza vedere [categorie di componenti](component-categories.md).



| Interfaccia                                                              | Utilizzo                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Metodo IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))<br/>           | L'oggetto può salvare e caricare lo stato in una matrice di byte sequenziali a lunghezza fissa (in memoria).<br/>                                                                                                                                                                                                                                                    |
| [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/>                  | L'oggetto può salvare e caricare lo stato in un'istanza di [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) . I controlli che desiderano essere contrassegnati come inseribili come altri oggetti documento composito (per l'inserimento in contenitori non compatibili con il controllo) devono supportare questa interfaccia.<br/>                                                                                               |
| [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85))<br/> | L'oggetto può salvare e caricare lo stato come singole proprietà scritte in IPropertyBag che il contenitore implementa. Viene usato per la funzionalità Salva come testo in alcuni contenitori.<br/>                                                                                                                                                          |
| [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/>  | L'oggetto può salvare e caricare lo stato in un percorso denominato da un moniker. Il controllo chiama [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) per recuperare l'interfaccia di archiviazione necessaria, ad esempio [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/objidl/nn-objidl-ilockbytes), [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)e così via.<br/> |



 

Sebbene il supporto per [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) sia facoltativo, si consiglia vivamente come ottimizzazione per i contenitori con funzionalità di testo Salva come, ad esempio Visual Basic.

Ad eccezione di [**IPersistStream:: GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax), [**IPersistStreamInit:: GetSizeMax**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-getsizemax)e [**Metodo IPersistMemory:: GetSizeMax**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768208(v=vs.85)), tutti i metodi di ogni interfaccia devono essere implementati completamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli](controls.md)
</dt> </dl>

 

