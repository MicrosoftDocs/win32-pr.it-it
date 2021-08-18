---
description: Un processo in due passaggi estende il Windows di transazione del programma di installazione ai prodotti contenenti assembly Common Language Runtime. In questo modo il programma di installazione può eseguire il rollback di installazioni e rimozioni di assembly non completate.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Rollback degli assembly nella Global Assembly Cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1379d8132e4a0789108bae4b26fc02c492f5ccb9a0ec7699bba3d9d4de04d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625826"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a>Rollback degli assembly nella Global Assembly Cache

Un processo in due passaggi estende il Windows di transazione del programma di installazione ai prodotti contenenti assembly Common Language Runtime. In questo modo il programma di installazione può eseguire il rollback di installazioni e rimozioni di assembly non completate.

Durante il primo passaggio, il programma di Windows usa Microsoft .NET Framework per creare un'interfaccia per ogni assembly. Il Windows di installazione usa tutte le interfacce di quanti sono gli assembly installati. Il commit di un assembly tramite una di queste interfacce significa solo che l'assembly è pronto per sostituire qualsiasi assembly esistente con lo stesso nome, non lo sostituisce ancora. Se l'utente annulla l'installazione o se si verifica un errore irreversibile di installazione, il programma di installazione di Windows può comunque eseguire il rollback dell'assembly allo stato precedente rilasciando queste interfacce.

Al termine dell Windows installazione di tutti gli assembly e dei componenti Windows Installer, il programma di installazione può avviare il secondo passaggio dell'installazione. Il secondo passaggio usa una funzione separata per eseguire il commit finale di tutti i nuovi assembly Common Language Runtime. In questo modo tutti gli assembly esistenti vengono sostituiti con lo stesso nome.

 

 



