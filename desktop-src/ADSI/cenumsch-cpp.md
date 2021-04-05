---
title: CENUMSCH. CPP
description: Nel componente provider di esempio, l'enumerazione di un oggetto dello schema utilizza i metodi, da cenumsch. cpp, elencati nella tabella seguente.
ms.assetid: edad1ad1-16b9-40f3-b841-a70aa7fff5d9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcc6d053bb698817ff73db876b00640ed00c8ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855345"
---
# <a name="cenumschcpp"></a>CENUMSCH. CPP

Nel componente provider di esempio, l'enumerazione di un oggetto dello schema utilizza i metodi, da cenumsch. cpp, elencati nella tabella seguente.



| Metodo                                        | Descrizione                                                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **CSampleDSSchemaEnum:: create**               | Creare un oggetto per consentire l'enumerazione di un oggetto classe di schema ADSI.                                                |
| **CSampleDSSchemaEnum::CSampleDSSchemaEnum**  | Costruttore standard.                                                                                                |
| **CSampleDSSchemaEnum:: ~ CSampleDSSchemaEnum** | Distruttore standard.                                                                                                 |
| **CSampleDSSchemaEnum:: Next**                 | Recupera il numero specificato di elementi dall'oggetto dello schema indicato.                                          |
| **CSampleDSSchemaEnum:: EnumObjects**          | Gestire il recupero dei puntatori di interfaccia agli oggetti del tipo di oggetto indicato.                               |
| **CSampleDSSchemaEnum:: EnumObjects**          | Gestire il recupero dei puntatori di interfaccia agli oggetti del tipo di oggetto predefinito.                                  |
| **CSampleDSSchemaEnum::EnumClasses**          | Gestire il recupero dei puntatori di interfaccia solo agli oggetti della classe di schema contenuti in questo oggetto.                  |
| **CSampleDSSchemaEnum:: GetClassObject**       | Recuperare la definizione della classe dello schema successiva; Se trovato, creare un oggetto classe di schema e restituire il puntatore a interfaccia. |
| **CSampleDSSchemaEnum:: EnumProperties**       | Gestire il recupero dei puntatori di interfaccia agli oggetti proprietà contenuti solo in questo oggetto.                      |
| **CSampleDSSchemaEnum:: GetPropertyObject**    | Recuperare la definizione di proprietà successiva. Se trovato, creare un oggetto classe di schema e restituire il puntatore a interfaccia.     |
| **CSampleDSSchemaEnum::EnumSyntaxes**         | Gestire il recupero dei puntatori di interfaccia agli oggetti della sintassi contenuti solo in questo oggetto.                        |
| **CSampleDSSchemaEnum::GetSyntaxObject**      | Recuperare la definizione della sintassi successiva; Se trovato, creare un oggetto classe di schema e restituire il puntatore a interfaccia.       |



 

 

 




