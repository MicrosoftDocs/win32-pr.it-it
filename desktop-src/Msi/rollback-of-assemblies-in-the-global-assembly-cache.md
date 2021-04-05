---
description: Un processo in due passaggi estende il modello di transazione Windows Installer ai prodotti contenenti Common Language Runtime assembly. Ciò consente al programma di installazione di eseguire il rollback di installazioni e rimozioni non riuscite degli assembly.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Rollback degli assembly nella global assembly cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84bc3107355cb50c17043ee571edff708ba3f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751119"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a>Rollback degli assembly nella global assembly cache

Un processo in due passaggi estende il modello di transazione Windows Installer ai prodotti contenenti Common Language Runtime assembly. Ciò consente al programma di installazione di eseguire il rollback di installazioni e rimozioni non riuscite degli assembly.

Durante il primo passaggio, il Windows Installer utilizza il Framework Microsoft .NET per creare un'interfaccia per ogni assembly. Il Windows Installer utilizza il numero di interfacce disponibili per l'installazione degli assembly. Il commit di un assembly tramite una di queste interfacce significa solo che l'assembly è pronto per sostituire qualsiasi assembly esistente con lo stesso nome, ma non lo sostituisce. Se l'utente annulla l'installazione o se si verifica un errore di installazione irreversibile, il Windows Installer può comunque eseguire il rollback dell'assembly allo stato precedente rilasciando tali interfacce.

Al termine Windows Installer dell'installazione di tutti gli assembly e dei componenti Windows Installer, il programma di installazione può avviare il secondo passaggio dell'installazione. Il secondo passaggio usa una funzione separata per eseguire il commit finale di tutti i nuovi assembly di Common Language Runtime. Vengono sostituiti tutti gli assembly esistenti con lo stesso nome.

 

 



