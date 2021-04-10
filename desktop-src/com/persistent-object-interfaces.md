---
title: Interfacce oggetto permanenti (COM)
description: Un oggetto persistente implementa una o più interfacce oggetto permanenti.
ms.assetid: 8c8e44e4-f564-4af5-9a8a-ac6883862cae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df8920f1242d077044654d1090adcc0e3f3f05c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963514"
---
# <a name="persistent-object-interfaces"></a>Interfacce oggetto permanenti

Un oggetto persistente implementa una o più *interfacce oggetto permanenti*. I client utilizzano interfacce oggetto permanenti per indicare gli oggetti quando e dove archiviare il proprio stato. Tutte le interfacce di oggetti permanenti sono derivate da [**IPersist**](/windows/desktop/api/ObjIdl/nn-objidl-ipersist), pertanto qualsiasi oggetto che implementa qualsiasi interfaccia di oggetto persistente implementa anche **IPersist**.

Sono attualmente definite le seguenti interfacce oggetto permanenti:

-   [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)
-   [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)
-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)
-   [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))
-   [Metodo IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))
-   [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))

Gli implementatori scelgono le interfacce oggetto permanenti supportate da un oggetto a seconda della modalità di utilizzo dell'oggetto. Poiché non supporta le interfacce di oggetti persistenti, l'implementatore sta affermando che lo stato di questo oggetto non può essere archiviato in modo permanente. Grazie al supporto di una o più interfacce di oggetti persistenti, l'implementatore sta affermando che lo stato di questo oggetto può essere archiviato in modo permanente in uno o più supporti di archiviazione dati.

Nella tabella seguente sono elencati, ad esempio, diversi tipi di oggetto che consentono il supporto di interfacce di oggetti persistenti diverse.



| Category                            | Le interfacce oggetto permanenti sono in genere supportate                                                                                                                                                         |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Moniker<br/>                 | [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)<br/>                                                                                                                                                      |
| Oggetti incorporabili OLE<br/>   | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |
| Controlli ActiveX<br/>         | [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), Metodo IPersistMemory, IPersistPropertyBag, [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/> |
| Oggetti documento ActiveX<br/> | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |



 

Gli implementatori client possono inoltre scegliere le interfacce oggetto permanenti che il client può utilizzare. Le interfacce utilizzate da un client sono in genere determinate dalla posizione in cui il client può archiviare i propri dati. Un client in grado di archiviare solo i dati in un file flat utilizzerà probabilmente solo [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))e IPersistPropertyBag. (**IPersistStreamInit** può sostituire [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) nella maggior parte delle applicazioni, perché contiene tale definizione e aggiunge un metodo di inizializzazione). Un client in grado di salvare i dati in un file di archiviazione strutturata utilizzerà inoltre [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Inizializzazione di oggetti permanenti](initializing-persistent-objects.md)
</dt> </dl>

 

