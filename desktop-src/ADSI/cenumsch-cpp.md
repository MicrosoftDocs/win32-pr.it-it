---
title: CENUMSCH. CPP
description: Nel componente provider di esempio l'enumerazione di un oggetto schema usa i metodi di cenumsch.cpp elencati nella tabella seguente.
ms.assetid: edad1ad1-16b9-40f3-b841-a70aa7fff5d9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b9be8a58f2d3775f11f85f590f374fc67902a73891484c57e5756645390fda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840521"
---
# <a name="cenumschcpp"></a>CENUMSCH. CPP

Nel componente provider di esempio l'enumerazione di un oggetto schema usa i metodi di cenumsch.cpp elencati nella tabella seguente.



| Metodo                                        | Descrizione                                                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **CSampleDSSchemaEnum::Create**               | Creare un oggetto per consentire l'enumerazione di un oggetto classe dello schema ADSI.                                                |
| **CSampleDSSchemaEnum::CSampleDSSchemaEnum**  | Costruttore standard.                                                                                                |
| **CSampleDSSchemaEnum::~CSampleDSSchemaEnum** | Distruttore standard.                                                                                                 |
| **CSampleDSSchemaEnum::Next**                 | Recuperare il numero specificato di elementi dall'oggetto schema indicato.                                          |
| **CSampleDSSchemaEnum::EnumObjects**          | Gestire il recupero dei puntatori delle interfacce agli oggetti del tipo di oggetto indicato.                               |
| **CSampleDSSchemaEnum::EnumObjects**          | Gestire il recupero dei puntatori a interfaccia agli oggetti del tipo di oggetto predefinito.                                  |
| **CSampleDSSchemaEnum::EnumClasses**          | Gestire il recupero dei puntatori a interfaccia solo agli oggetti della classe dello schema contenuti in questo oggetto.                  |
| **CSampleDSSchemaEnum::GetClassObject**       | Recuperare la definizione della classe dello schema successiva. Se viene trovato, creare un oggetto classe dello schema e restituire il puntatore a interfaccia. |
| **CSampleDSSchemaEnum::EnumProperties**       | Gestire il recupero dei puntatori a interfaccia agli oggetti proprietà contenuti solo in questo oggetto.                      |
| **CSampleDSSchemaEnum::GetPropertyObject**    | Recuperare la definizione della proprietà successiva. Se viene trovato, creare un oggetto classe dello schema e restituire il puntatore a interfaccia.     |
| **CSampleDSSchemaEnum::EnumSyntaxes**         | Gestire il recupero dei puntatori a interfaccia agli oggetti sintassi contenuti solo in questo oggetto.                        |
| **CSampleDSSchemaEnum::GetSyntaxObject**      | Recuperare la definizione della sintassi successiva. Se viene trovato, creare un oggetto classe dello schema e restituire il puntatore a interfaccia.       |



 

 

 




