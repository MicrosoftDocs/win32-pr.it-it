---
title: GETOBJ. CPP
description: Nel componente provider di esempio viene visualizzato un esempio di codice usato per trovare e associare oggetti in Getobj. cpp. Le routine supportate sono elencate nella tabella seguente.
ms.assetid: d202e5ec-27b5-4809-a7fa-4a2e39c65295
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d58647208c68437c068d58cd9908bc08989141
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339246"
---
# <a name="getobjcpp"></a>GETOBJ. CPP

Nel componente provider di esempio viene visualizzato un esempio di codice usato per trovare e associare oggetti in Getobj. cpp. Le routine supportate sono elencate nella tabella seguente.



| Elemento                                | Descrizione                                                                                                                                                                                                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RelativeGetObject**               | Ottiene un oggetto relativo a un ADsPath specificato.                                                                                                                                                                                                                                                       |
| **GetObject**                       | Chiama **ADsObject** (Parse. cpp) per verificare la sintassi del percorso, verifica che il percorso disponga del token del provider corretto e convalidare il tipo di oggetto. Se non sono presenti errori, creare un'istanza del tipo di oggetto corretto e recuperare un puntatore all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) dell'oggetto. |
| **BuildADsPathFromDSPath**          | Compilazione di una stringa ADsPath dal percorso della directory nativa.                                                                                                                                                                                                                                           |
| **BuildDSTreeNameFromADsPath**      | Usare ADsPath per creare un possibile percorso di directory dell'albero per il percorso della directory nativa.                                                                                                                                                                                                           |
| **BuildDSPathFromADsPath**          | USA ADsPath e DSPathName.                                                                                                                                                                                                                                                                      |
| **BuildADsParentPath**              | Compilare ADsPath nell'elemento padre per questo oggetto.                                                                                                                                                                                                                                                  |
| **GetNamespaceObject**              | Convalidare e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) un oggetto spazio dei nomi di esempio.                                                                                                                                                                                                           |
| **ValidateNamespaceObject**         | Verificare che l'oggetto dello spazio dei nomi corrisponda al nome del provider corrente.                                                                                                                                                                                                                               |
| **ValidateProvider**                | Convalida il nome del provider (con distinzione tra maiuscole e minuscole).                                                                                                                                                                                                                                                          |
| **GetSchemaObject**                 | Convalidare e aprire il tipo di oggetto dello schema appropriato. Quindi, creare quello corretto e recuperare il puntatore all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .                                                                                                                                        |
| **ValidateSchemaObject**            | Verificare che si tratta di un tipo di oggetto schema valido.                                                                                                                                                                                                                                                     |
| **ValidateObjectType**              | Verificare che il tipo di oggetto esista nello schema.                                                                                                                                                                                                                                                 |
| **BuildSampleDSRootRDNFromADsPath** | Compilare ADsPath nel nodo radice per il componente provider di esempio.                                                                                                                                                                                                                            |
| **BuildDSPathFromADsPath**          | USA ADsPath, DSRootRDN e DSPathName.                                                                                                                                                                                                                                                          |



 

 

 