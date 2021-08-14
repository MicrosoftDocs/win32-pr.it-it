---
title: CPROPS. CPP
description: Nel componente provider di esempio un esempio di implementazione della cache delle proprietà è disponibile in cprops.cpp. I metodi supportati sono elencati nella tabella seguente.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66394b7375779f50a97505128178ec35106187c076ca5d6741375a7f71b8ec46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429000"
---
# <a name="cpropscpp"></a>CPROPS. CPP

Nel componente provider di esempio un esempio di implementazione della cache delle proprietà è disponibile in cprops.cpp. I metodi supportati sono elencati nella tabella seguente.



| Metodo                                           | Descrizione                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **CPropertyCache::addproperty**                  | Estendere la cache delle proprietà aggiungendo una nuova.                                                                      |
| **CPropertyCache::updateproperty**               | Cercare la proprietà, liberarne il contenuto e usare invece nuovi valori. contrassegnare quindi la cache modificata per questa proprietà. |
| **CPropertyCache::findproperty**                 | Cercare questa proprietà in base al nome. salvare l'indice.                                                                      |
| **CPropertyCache::getproperty**                  | Trovare la proprietà nella cache, se disponibile, in caso contrario chiamare **GetInfo**. Impostare l'indice e copiarlo nei nuovi valori.  |
| **CPropertyCache::p utproperty**                  | Trovare la proprietà . Liberare ciò che c'era e inserire nuovi valori.                                                       |
| **CPropertyCache::CPropertyCache**               | Costruttore standard.                                                                                               |
| **CPropertyCache::~CPropertyCache**              | Distruttore standard.                                                                                                |
| **CPropertyCache::createpropertycache**          | Creare la cache.                                                                                                   |
| **CPropertyCache::unboundgetproperty**           | Trovare la proprietà nella cache e impostarla su questi valori.                                                          |
| **CPropertyCache::SampleDSMarshallProperties**   | Effettuare il marshalling dei dati e dei valori delle proprietà.                                                                                   |
| **CPropertyCache::marshallproperty**             | Effettuare il marshalling di una proprietà.                                                                                                 |
| **CPropertyCache::SampleDSUnMarshallProperties** | Dati e valori delle proprietà unmarshal.                                                                                 |
| **CPropertyCache::unmarshallproperty**           | Annullare ilmarshal di una proprietà.                                                                                               |



 

 

 




