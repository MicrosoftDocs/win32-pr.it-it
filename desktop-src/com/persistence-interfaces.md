---
title: Interfacce di persistenza
description: Interfacce di persistenza
ms.assetid: a93582b3-bdbf-430d-b4a6-c0df7bc35dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e1acbd1074fd5fa4e87e571a1e21ab48d5d075
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550506"
---
# <a name="persistence-interfaces"></a>Interfacce di persistenza

Gli oggetti con uno stato permanente di qualsiasi tipo devono implementare almeno un'interfaccia IPersist e preferibilmente più interfacce, per fornire al contenitore la scelta più flessibile di come desidera salvare lo stato di un \* controllo.

Se un controllo ha qualsiasi stato permanente, deve, come minimo, implementare [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) (i due si escludono a vicenda e non devono essere implementati insieme per la maggior parte). Quest'ultimo viene usato quando un controllo vuole sapere quando viene creato nuovo anziché ricaricarlo da uno stato permanente esistente (**IPersistStream** non ha la nuova funzionalità creata). L'esistenza di una delle due interfacce indica che il controllo può salvare e caricare il relativo stato permanente in un flusso, ad esempio un'istanza di [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).

Oltre a queste due interfacce basate su flusso, è possibile specificare facoltativamente le interfacce IPersist elencate nella tabella seguente per supportare la persistenza in posizioni diverse da un \* [**IStream espandibile.**](/windows/desktop/api/objidl/nn-objidl-istream)

Viene identificato un set di categorie di componenti per coprire il supporto per le interfacce di persistenza, vedere [Categorie di componenti](component-categories.md).



| Interfaccia                                                              | Utilizzo                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ipersistmemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))<br/>           | L'oggetto può salvare e caricare lo stato in una matrice di byte sequenziale a lunghezza fissa (in memoria).<br/>                                                                                                                                                                                                                                                    |
| [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/>                  | L'oggetto può salvare e caricare il relativo stato in [**un'istanza di IStorage.**](/windows/desktop/api/objidl/nn-objidl-istorage) I controlli che desiderano essere contrassegnati come inseriscibili come altri oggetti documento compositi (per l'inserimento in contenitori non in grado di riconoscere i controlli) devono supportare questa interfaccia.<br/>                                                                                               |
| [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)<br/> | L'oggetto può salvare e caricare il relativo stato come singole proprietà scritte in IPropertyBag implementate dal contenitore. Viene usato per la funzionalità Salva come testo in alcuni contenitori.<br/>                                                                                                                                                          |
| [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/>  | L'oggetto può salvare e caricare lo stato in un percorso denominato da un moniker. Il controllo chiama [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) per recuperare l'interfaccia di archiviazione necessaria, ad esempio [**IStorage,**](/windows/desktop/api/objidl/nn-objidl-istorage) [**IStream,**](/windows/desktop/api/objidl/nn-objidl-istream) [**ILockBytes,**](/windows/desktop/api/objidl/nn-objidl-ilockbytes) [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)e così via.<br/> |



 

Anche se il [**supporto per IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) è facoltativo, è fortemente consigliato come ottimizzazione per i contenitori con funzionalità Salva come testo, ad esempio Visual Basic.

Ad eccezione di [**IPersistStream::GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax), [**IPersistStreamInit::GetSizeMax**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-getsizemax)e [**IPersistMemory::GetSizeMax**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768208(v=vs.85)), tutti i metodi di ogni interfaccia devono essere completamente implementati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli](controls.md)
</dt> </dl>

 

