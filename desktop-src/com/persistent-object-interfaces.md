---
title: Interfacce COM (Persistent Object Interface)
description: Un oggetto persistente implementa una o più interfacce oggetto persistenti.
ms.assetid: 8c8e44e4-f564-4af5-9a8a-ac6883862cae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ee1062c80a5c40d139965e0e3bebf96cbda534062322e218e2f5a7da586ff0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120411"
---
# <a name="persistent-object-interfaces"></a>Interfacce di oggetti persistenti

Un oggetto persistente implementa una o più *interfacce oggetto persistenti.* I client usano interfacce di oggetti persistenti per indicare a tali oggetti quando e dove archiviarne lo stato. Tutte le interfacce di oggetti persistenti derivano da [**IPersist,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersist)pertanto qualsiasi oggetto che implementa qualsiasi interfaccia di oggetti persistenti implementa **anche IPersist.**

Le interfacce degli oggetti persistenti seguenti sono attualmente definite:

-   [**Ipersiststream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)
-   [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)
-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)
-   [**Ipersistfile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)
-   [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))
-   [Ipersistmemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))
-   [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))

Gli implementatori scelgono le interfacce oggetto persistenti supportate da un oggetto a seconda della modalità di utilizzo dell'oggetto. Non supportando alcuna interfaccia oggetto persistente, l'implementatore dice in modo efficace che "Lo stato di questo oggetto non può essere archiviato in modo permanente". Supportando una o più interfacce oggetto persistenti, l'implementatore afferma in modo efficace che lo stato di questo oggetto può essere archiviato in modo permanente in uno o più supporti di archiviazione dati.

Nella tabella seguente, ad esempio, sono elencati diversi tipi di oggetto che consentono il supporto per diverse interfacce di oggetti persistenti.



| Category                            | Interfacce di oggetti persistenti in genere supportate                                                                                                                                                         |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Moniker<br/>                 | [**Ipersiststream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)<br/>                                                                                                                                                      |
| Oggetti incorporabili OLE<br/>   | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |
| Controlli ActiveX<br/>         | [**IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), IPersistMemory, IPersistPropertyBag, [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/> |
| ActiveX oggetti documento<br/> | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |



 

Gli implementatori del client possono anche scegliere quali interfacce di oggetti persistenti possono essere usate dal client. Le interfacce utilizzate da un client sono in genere determinate dalla posizione in cui il client può archiviare i propri dati. Un client in grado di archiviare i dati solo in un file flat userà probabilmente solo [**IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))e IPersistPropertyBag. (**IPersistStreamInit** può sostituire [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) nella maggior parte delle applicazioni, perché contiene tale definizione e aggiunge un metodo di inizializzazione. Un client in grado di salvare i dati in un file di archiviazione strutturata userà anche [**IPersistStorage.**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Inizializzazione di oggetti persistenti](initializing-persistent-objects.md)
</dt> </dl>

 

