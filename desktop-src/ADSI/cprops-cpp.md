---
title: CPROPS. CPP
description: Nel componente provider di esempio, è possibile trovare un esempio di implementazione della cache delle proprietà in cProps. cpp. I metodi supportati sono elencati nella tabella seguente.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b9f4fddfea6900fd8d7a06bee9979744eefd30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855333"
---
# <a name="cpropscpp"></a>CPROPS. CPP

Nel componente provider di esempio, è possibile trovare un esempio di implementazione della cache delle proprietà in cProps. cpp. I metodi supportati sono elencati nella tabella seguente.



| Metodo                                           | Descrizione                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **CPropertyCache:: AddProperty**                  | Estendere la cache delle proprietà aggiungendone una nuova.                                                                      |
| **CPropertyCache:: UpdateProperty**               | Cercare la proprietà, liberarne il contenuto e usare invece i nuovi valori; contrassegnare quindi la cache modificata per questa proprietà. |
| **CPropertyCache:: FindProperty**                 | Cercare questa proprietà in base al nome; salvare il relativo indice.                                                                      |
| **CPropertyCache:: GetProperty**                  | Trovare la proprietà nella cache, se disponibile, in caso contrario chiamare **GetInfo**. Impostare l'indice e copiare i nuovi valori.  |
| **CPropertyCache::p utproperty**                  | Trovare la proprietà. Liberare le informazioni disponibili e inserire i nuovi valori.                                                       |
| **CPropertyCache:: CPropertyCache**               | Costruttore standard.                                                                                               |
| **CPropertyCache:: ~ CPropertyCache**              | Distruttore standard.                                                                                                |
| **CPropertyCache:: createpropertycache**          | Creare la cache.                                                                                                   |
| **CPropertyCache:: unboundgetproperty**           | Trovare la proprietà nella cache e impostarla su questi valori.                                                          |
| **CPropertyCache:: SampleDSMarshallProperties**   | Eseguire il marshalling dei dati e dei valori delle proprietà.                                                                                   |
| **CPropertyCache:: marshallproperty**             | Eseguire il marshalling di una proprietà.                                                                                                 |
| **CPropertyCache:: SampleDSUnMarshallProperties** | Annullare il marshalling dei dati e dei valori delle proprietà.                                                                                 |
| **CPropertyCache:: unmarshallproperty**           | Annullare il marshalling di una proprietà.                                                                                               |



 

 

 




