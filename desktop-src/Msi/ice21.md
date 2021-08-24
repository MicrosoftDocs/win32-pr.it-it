---
description: ICE21 verifica che ogni componente nella tabella Component appartenga a una funzionalità. Usa la tabella FeatureComponents per verificare la presenza di questo mapping.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c5c517bd41c7d777f327606b3672f90b57a821dbbef028fa985acd043e6768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529031"
---
# <a name="ice21"></a>ICE21

ICE21 verifica che ogni componente nella tabella [Component](component-table.md) appartenga a una funzionalità. Usa la tabella [FeatureComponents per](featurecomponents-table.md) verificare la presenza di questo mapping.

## <a name="result"></a>Risultato

ICE21 invia un messaggio di errore se il pacchetto di installazione contiene un componente che non appartiene a una funzionalità.

## <a name="example"></a>Esempio

Per l'esempio seguente, ICE21 pubblica un messaggio di errore che indica che il componente Comp1 non è mappato ad alcuna funzionalità.

[Tabella dei componenti](component-table.md) (parziale)



| Componente |
|-----------|
| Comp1     |
| Comp2     |



 

[Tabella FeatureComponents](featurecomponents-table.md) (parziale)



| Funzionalità  | Componente |
|----------|-----------|
| Funzionalità1 | Comp2     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



