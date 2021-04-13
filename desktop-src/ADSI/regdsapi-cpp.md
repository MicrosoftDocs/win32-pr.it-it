---
title: REGDSAPI. CPP
description: Nel componente provider di esempio, le funzioni che rappresentano un'API che accede direttamente al sistema operativo nativo si trovano in Regdsapi. cpp.
ms.assetid: dc5ab286-5c70-43a3-90a1-f3f8a1c61c43
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e160ab212960753c6f793f734ebd96dffdd0f9e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328375"
---
# <a name="regdsapicpp"></a>REGDSAPI. CPP

Nel componente provider di esempio, le funzioni che rappresentano un'API che accede direttamente al sistema operativo nativo si trovano in Regdsapi. cpp. Il componente provider di esempio implementa il servizio directory nel registro di sistema. Per scrivere un provider che accede al proprio servizio directory, creare implementazioni personalizzate dell'API. Le funzioni supportate sono elencate nella tabella seguente.



| Metodo                             | Descrizione                                                                                                                                                                                    |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SampleDSOpenObject**             | Aprire l'oggetto in base al nome. Se il parametro di tipo della classe dello schema è **null**, compilare il tipo trovato. Recuperare un handle per l'oggetto.                                                             |
| **SampleDSCloseObject**            | Usare l'handle recuperato da **SampleDSOpenObject**.                                                                                                                                            |
| **SampleDSRDNEnum**                | Recuperare l'handle su un oggetto enumeratore per gestire l'enumerazione dei nomi distinti relativi (RDNs) da un oggetto contenitore.                                                          |
| **SampleDSNextRDN**                | Usando l'handle recuperato da **SampleDSRDNEnum**, ottenere il nome distinto relativo successivo da questo oggetto contenitore.                                                                        |
| **SampleDSFreeEnum**               | Liberare l'oggetto enumeratore allocato in **SampleDSRDNEnum**.                                                                                                                                   |
| **SampleDSModifyObject**           | Modificare le proprietà di un oggetto nel servizio directory in base all'handle dell'oggetto e a un elenco di attributi e ai relativi valori.                                                              |
| **SampleDSReadObject**             | Leggere le proprietà dell'oggetto dal servizio directory. Eseguire il mapping della sintassi dall'archiviazione nativa ai valori di sintassi degli annunci appropriati. Gestire le proprietà con più valori di conseguenza. |
| **SampleDSGetPropertyDefinition**  | Nello schema cercare tutte le definizioni di proprietà e i relativi attributi per questo tipo di oggetto classe di schema.                                                                                     |
| **SampleDSGetPropertyDefinition**  | Nello schema cercare questa proprietà e i relativi attributi in base al nome.                                                                                                                               |
| **SampleDSFreePropertyDefinition** | Memoria libera allocata da **GetPropertyDefinition**.                                                                                                                                            |
| **SampleDSGetTypeText**            | Ottenere il tipo di classe dello schema di un oggetto in formato testo.                                                                                                                                         |
| **SampleDSGetType**                | Ottiene il tipo di classe dello schema di un oggetto.                                                                                                                                                        |
| **SampleDSGetPropertyInfo**        | Dato un handle per l'oggetto classe di schema e un nome di proprietà, recuperare le informazioni sulle proprietà, ad esempio la sintassi e così via.                                                                      |
| **FreeList**                       | Liberare la memoria usata da un elenco di LPWSTR \_ .                                                                                                                                                        |
| **SampleDSGetClassDefinition**     | Recuperare il set di tutte le definizioni delle classi dello schema e i dati associati dallo schema.                                                                                                    |
| **SampleDSGetClassDefinition**     | Recuperare i dati relativi a una particolare classe di schema nello schema.                                                                                                                                   |
| **SampleDSGetClassInfo**           | Dato il nome di una classe di schema, cercare i dati associati, ad esempio le proprietà obbligatorie.                                                                                                      |
| **SampleDSAddObject**              | Aggiungere un oggetto nel servizio directory.                                                                                                                                                        |
| **SampleDSRemoveObject**           | Rimuovere un oggetto dal servizio directory.                                                                                                                                                   |
| **SampleDSCreateBuffer**           | Creare un buffer di memoria per i dati dell'attributo e i dati dell'operazione.                                                                                                                                  |
| **SampleDSFreeBuffer**             | Liberare il buffer creato in **SampleDSCreateBuffer**.                                                                                                                                           |



 

 

 




