---
title: CPRPOBJ. CPP
description: Nel componente provider di esempio i metodi dell'oggetto proprietà in cprpobj.cpp sono elencati nella tabella seguente.
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb130d6deced939aa718e839c0e7f178329e6a5b14c383dbf1a2719c0f25cfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840335"
---
# <a name="cprpobjcpp"></a>CPRPOBJ. CPP

Nel componente provider di esempio i metodi dell'oggetto proprietà in cprpobj.cpp sono elencati nella tabella seguente.



| Metodo                                                 | Descrizione                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSProperty::CSampleDSProperty**               | Costruttore standard.                                                                                                                          |
| **CSampleDSProperty::~CSampleDSProperty**              | Distruttore standard.                                                                                                                           |
| **CSampleDSProperty::CreateProperty**                  | Creare un oggetto Proprietà ADS, cercando le definizioni degli attributi chiamando **SampleDSGetPropertyDefinition.**                              |
| **CSampleDSProperty::CreateProperty**                  | Data la definizione dell'attributo, creare un oggetto proprietà, impostando la corrispondenza tra le sintassi DIS supportate e le sintassi del provider. |
| **CSampleDSProperty::AllocatePropertyObject**          | Creare un oggetto proprietà e caricarne i dati di tipo.                                                                                               |
| **CSampleDSProperty::QueryInterface**                  | Restituisce il puntatore a interfaccia richiesto, se disponibile.                                                                                          |
| Metodi [**IAD**](/windows/desktop/api/Iads/nn-iads-iads) standard.                 |                                                                                                                                                |
| Metodi [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) standard. |                                                                                                                                                |
| **MapSyntaxIdtoADsSyntax**                             | Impostare la corrispondenza tra l'ID sintassi e la sintassi di ADS.                                                                               |
| **MapSyntaxIdtoSampleDSSyntax**                        | Impostare la corrispondenza tra l'ID sintassi e la sintassi del provider.                                                                          |



 

 

 




