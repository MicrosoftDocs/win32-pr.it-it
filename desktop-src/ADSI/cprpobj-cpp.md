---
title: CPRPOBJ. CPP
description: Nel componente provider di esempio, i metodi dell'oggetto Property, in cprpobj. cpp, sono elencati nella tabella seguente.
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948409cc135daaffa249f8aa0b3729b34799957c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220919"
---
# <a name="cprpobjcpp"></a>CPRPOBJ. CPP

Nel componente provider di esempio, i metodi dell'oggetto Property, in cprpobj. cpp, sono elencati nella tabella seguente.



| Metodo                                                 | Descrizione                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSProperty::CSampleDSProperty**               | Costruttore standard.                                                                                                                          |
| **CSampleDSProperty:: ~ CSampleDSProperty**              | Distruttore standard.                                                                                                                           |
| **CSampleDSProperty:: CreateProperty**                  | Creare un oggetto proprietà ADS, cercando le definizioni degli attributi chiamando **SampleDSGetPropertyDefinition**.                              |
| **CSampleDSProperty:: CreateProperty**                  | Data la definizione dell'attributo, creare un oggetto Property, impostando la corrispondenza tra le sintassi degli annunci supportati e le sintassi del provider. |
| **CSampleDSProperty::AllocatePropertyObject**          | Creare un oggetto proprietà e caricarne i dati di tipo.                                                                                               |
| **CSampleDSProperty:: QueryInterface**                  | Restituisce il puntatore a interfaccia richiesto, se disponibile.                                                                                          |
| Metodi [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) standard.                 |                                                                                                                                                |
| Metodi [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) standard. |                                                                                                                                                |
| **MapSyntaxIdtoADsSyntax**                             | Impostare la corrispondenza tra l'ID sintassi e la sintassi ADS.                                                                               |
| **MapSyntaxIdtoSampleDSSyntax**                        | Impostare la corrispondenza tra l'ID sintassi e la sintassi del provider.                                                                          |



 

 

 




