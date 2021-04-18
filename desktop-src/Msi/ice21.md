---
description: ICE21 verifica che ogni componente della tabella dei componenti appartenga a una funzionalità. Usa la tabella FeatureComponents per verificare il mapping.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c457d026b3dc57a718eabea704254a3448a3de26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314230"
---
# <a name="ice21"></a>ICE21

ICE21 verifica che ogni componente della tabella dei [componenti](component-table.md) appartenga a una funzionalità. Usa la [tabella FeatureComponents](featurecomponents-table.md) per verificare il mapping.

## <a name="result"></a>Risultato

ICE21 Invia un messaggio di errore se il pacchetto di installazione contiene un componente che non appartiene a una funzionalità.

## <a name="example"></a>Esempio

Per l'esempio seguente, ICE21 Invia un messaggio di errore che informa che il componente comp1 non è mappato ad alcuna funzionalità.

[Tabella componenti](component-table.md) (parziale)



| Componente |
|-----------|
| Comp1     |
| Comp2     |



 

[Tabella FeatureComponents](featurecomponents-table.md) (parziale)



| Funzionalità  | Componente |
|----------|-----------|
| Feature1 | Comp2     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



