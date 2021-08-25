---
description: I moduli unione richiedono raramente un'interfaccia utente.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Creazione di interfacce utente nei moduli unione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931e539d8880c490853b20a6e53b3000f390c0b29f81bf8bb9d3e3703e3f7905
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829191"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a>Creazione di interfacce utente nei moduli unione

I moduli unione richiedono raramente un'interfaccia utente. Il rilascio di un modulo unione che contiene sia componenti installabili che un'interfaccia utente limita infine la flessibilità dell'utente del modulo. La combinazione di componenti e interfaccia utente in un unico modulo può impedire agli sviluppatori di usare la propria interfaccia utente o di fornire installazioni invisibile all'utente. Un'alternativa migliore consiste nel rilasciare due moduli unione, uno che installa automaticamente i componenti e un secondo modulo facoltativo che contiene l'interfaccia utente. Il modulo con l'interfaccia utente dovrebbe elencare il modulo componente nella [relativa tabella ModuleDependency](moduledependency-table.md). Questo metodo consente agli autori di moduli di fornire un'interfaccia utente senza forzarla agli sviluppatori.

Quando le tabelle dell'interfaccia utente vengono usate nei moduli unione, possono essere unite nello stesso modo di qualsiasi altra tabella.

 

 



