---
title: Interfacce private Container-Specific
description: Interfacce private Container-Specific
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c6569a79e9f1801c6fd82543bc40408903c780
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332359"
---
# <a name="container-specific-private-interfaces"></a>Interfacce private Container-Specific

Alcuni contenitori forniscono interfacce private specifiche del contenitore per funzionalità aggiuntive o prestazioni migliori. I controlli basati su tali interfacce specifiche del contenitore dovrebbero, se possibile, funzionare senza le interfacce specifiche del contenitore presenti, in modo che il controllo funzioni in contenitori diversi. Ad esempio, Visual Basic implementa interfacce private che forniscono la funzionalità di formattazione delle stringhe ai controlli. Se un controllo Usa queste interfacce di formattazione privata, dovrebbe essere in grado di eseguire con il supporto predefinito per la formattazione se queste interfacce non sono disponibili. Se il controllo può funzionare senza le interfacce private, deve adottare un'azione appropriata, ad esempio avvisare l'utente di una funzionalità ridotta, ma continuare a lavorare. Se non si tratta di un'opzione, la categoria di un componente deve essere registrata come richiesto, in modo che solo i contenitori che supportano questa funzionalità possano ospitare tali controlli.

 

 




