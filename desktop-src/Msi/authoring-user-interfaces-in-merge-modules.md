---
description: I moduli merge richiedono raramente un'interfaccia utente.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Creazione di interfacce utente nei moduli merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2df8781efea35ddd854ef76c2155d4a2ded7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311028"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a>Creazione di interfacce utente nei moduli merge

I moduli merge richiedono raramente un'interfaccia utente. Il rilascio di un modulo merge che contiene entrambi i componenti installabili e un'interfaccia utente limita la flessibilità dell'utente del modulo. La combinazione di componenti e interfaccia utente in un modulo può impedire agli sviluppatori di usare la propria interfaccia utente o di fornire installazioni invisibili. Un'alternativa migliore consiste nel rilasciare due moduli unione, uno che installa automaticamente i componenti e un secondo modulo facoltativo che contiene l'interfaccia utente. Il modulo con l'interfaccia utente dovrebbe elencare il modulo Component nella [tabella ModuleDependency](moduledependency-table.md). Questo metodo consente agli autori di moduli di fornire un'interfaccia utente senza forzarla sugli sviluppatori.

Quando le tabelle dell'interfaccia utente vengono utilizzate nei modelli unione, possono essere unite allo stesso modo di qualsiasi altra tabella.

 

 



