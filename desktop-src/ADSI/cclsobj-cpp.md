---
title: CCLSOBJ. CPP
description: Nel componente provider di esempio, le funzioni per l'oggetto classe di schema sono contenute in cclsobj. cpp.
ms.assetid: e8cdef8e-c031-49e0-9496-871064aec8bd
ms.tgt_platform: multiple
keywords:
- CSampleDSClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23c198413819627ce1fcb5a605bd8e45faae0ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297695"
---
# <a name="cclsobjcpp"></a>CCLSOBJ. CPP

Nel componente provider di esempio, le funzioni per l'oggetto classe di schema sono contenute in cclsobj. cpp.

La classe **CSampleDSClass** è definita in questo file. **CSampleDSClass** viene definito con i metodi e le proprietà elencati nella tabella seguente.



| Metodo                      | Descrizione                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSClass**          | Costruttore standard.                                                                                                                                                                                      |
| **~ CSampleDSClass**         | Distruttore standard.                                                                                                                                                                                       |
| **CreateClass**             | Creare un oggetto classe di schema ADs. Definizioni degli attributi di ricerca chiamando **SampleDSGetClassDefinition**.                                                                                                 |
| **CreateClass**             | Creare un oggetto classe di schema, in base alle definizioni degli attributi, impostando attributi noti, ad esempio quelli elencati in [**IADsClass:: MandatoryAttributes**](iadsclass-property-methods.md).                     |
| **AllocateClassObject**     | Creare un oggetto classe di schema e caricarne i dati di tipo.                                                                                                                                                       |
| **QueryInterface**          | Restituisce il puntatore a interfaccia richiesto, se disponibile.                                                                                                                                                      |
| Metodi IADs standard.      | Metodi di interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) standard inclusi in questo file.                                                                                                                                     |
| Metodi IADsClass standard. | Metodi di interfaccia [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) standard inclusi in questo file.                                                                                                                           |
| **CreatePropertyList**      | Creare un elenco di proprietà associate a questa classe dello schema chiamando **CreatePropertyEntry**.                                                                                                          |
| **CreatePropertyEntry**     | Creare un oggetto proprietà in questa classe dello schema.                                                                                                                                                           |
| **FreePropertyEntry**       | Liberare la voce in **CreatePropertyEntry**.                                                                                                                                                            |
| **MakeVariantFromPropList** | Creare una matrice di varianti dall'elenco di proprietà creato da **CreatePropertyList**. Può essere usato nell'implementazione di [**IADsClass:: MandatoryAttributes**](iadsclass-property-methods.md) e così via. |



 

 

 




