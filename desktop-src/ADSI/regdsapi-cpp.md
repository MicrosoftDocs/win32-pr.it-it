---
title: REGDSAPI. CPP
description: Nel componente provider di esempio le funzioni che rappresentano un'API che accede direttamente al sistema operativo nativo sono in Regdsapi.cpp.
ms.assetid: dc5ab286-5c70-43a3-90a1-f3f8a1c61c43
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80179650c51f3561b8ab73bb5b28cd428867f7feac79a8341b315a1f2a510d93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119307661"
---
# <a name="regdsapicpp"></a>REGDSAPI. CPP

Nel componente provider di esempio le funzioni che rappresentano un'API che accede direttamente al sistema operativo nativo sono in Regdsapi.cpp. Il componente provider di esempio implementa il servizio directory nel Registro di sistema. Per scrivere un provider che accede al proprio servizio directory, creare le proprie implementazioni di questa API. Le funzioni supportate sono elencate nella tabella seguente.



| Metodo                             | Descrizione                                                                                                                                                                                    |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SampleDSOpenObject**             | Aprire questo oggetto in base al nome. Se il parametro del tipo della classe dello schema **è NULL,** compilare il tipo trovato. Recuperare un handle sull'oggetto .                                                             |
| **SampleDSCloseObject**            | Usare l'handle recuperato **da SampleDSOpenObject**.                                                                                                                                            |
| **SampleDSRDNEnum**                | Recuperare l'handle su un oggetto enumeratore per gestire l'enumerazione dei nomi distinti relativi (RDN) da un oggetto contenitore.                                                          |
| **SampleDSNextRDN**                | Usando l'handle recuperato da **SampleDSRDNEnum,** ottenere il nome distinto relativo successivo da questo oggetto contenitore.                                                                        |
| **SampleDSFreeEnum**               | Liberare l'oggetto enumeratore allocato in **SampleDSRDNEnum**.                                                                                                                                   |
| **SampleDSModifyObject**           | Modificare le proprietà di un oggetto nel servizio directory in base all'handle dell'oggetto e a un elenco di attributi e ai relativi valori.                                                              |
| **SampleDSReadObject**             | Leggere le proprietà dell'oggetto dal servizio directory. Eseguire il mapping della sintassi dall'archiviazione nativa ai valori di sintassi DIS appropriati. Gestire le proprietà con più valori di conseguenza. |
| **SampleDSGetPropertyDefinition**  | Nello schema cercare tutte le definizioni di proprietà e i relativi attributi per questo tipo di oggetto classe dello schema.                                                                                     |
| **SampleDSGetPropertyDefinition**  | Nello schema cercare questa proprietà e i relativi attributi in base al nome.                                                                                                                               |
| **SampleDSFreePropertyDefinition** | Memoria disponibile allocata da **GetPropertyDefinition.**                                                                                                                                            |
| **SampleDSGetTypeText**            | Ottiene il tipo di classe dello schema di un oggetto in formato testo.                                                                                                                                         |
| **SampleDSGetType**                | Ottiene il tipo di classe dello schema di un oggetto.                                                                                                                                                        |
| **SampleDSGetPropertyInfo**        | Dato un handle per l'oggetto della classe dello schema e un nome di proprietà, recuperare le informazioni sulle proprietà, ad esempio la sintassi e così via.                                                                      |
| **FreeList**                       | Liberare la memoria usata da un elenco LPWSTR. \_                                                                                                                                                        |
| **SampleDSGetClassDefinition**     | Recuperare il set di tutte le definizioni di classi dello schema e i dati associati dallo schema.                                                                                                    |
| **SampleDSGetClassDefinition**     | Recuperare i dati relativi a una determinata classe dello schema nello schema.                                                                                                                                   |
| **SampleDSGetClassInfo**           | Dato il nome di una classe di schema, cercare i dati associati, ad esempio le proprietà obbligatorie.                                                                                                      |
| **SampleDSAddObject**              | Aggiungere un oggetto nel servizio directory.                                                                                                                                                        |
| **SampleDSRemoveObject**           | Rimuovere un oggetto dal servizio directory.                                                                                                                                                   |
| **SampleDSCreateBuffer**           | Creare un buffer di memoria per i dati dell'attributo e i dati dell'operazione.                                                                                                                                  |
| **SampleDSFreeBuffer**             | Liberare il buffer creato in **SampleDSCreateBuffer**.                                                                                                                                           |



 

 

 




