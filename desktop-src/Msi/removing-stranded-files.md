---
description: Elenco dei possibili motivi per cui una disinstallazione di Windows Installer non è stata in grado di rimuovere tutti i file di un'applicazione.
ms.assetid: 0a856f0f-a829-478e-a83b-dade7b05b4f2
title: Rimozione di file bloccati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5eeceb45c2139d146c32bdf9917e41885688df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313799"
---
# <a name="removing-stranded-files"></a>Rimozione di file bloccati

Se un file che dovrebbe essere stato rimosso dal computer dell'utente rimane installato dopo l'esecuzione di una disinstallazione, il programma di installazione potrebbe non rimuovere il componente contenente il file per uno o più dei seguenti motivi:

-   Il bit msidbComponentAttributesPermanent è stato impostato per il componente nella colonna Attributes della [tabella Component](component-table.md).
-   Nessun valore immesso per il componente nella colonna ComponentId della tabella Component.
-   Il componente viene utilizzato da un'altra applicazione o funzionalità ancora installata.
-   Nella tabella della [condizione](condition-table.md) è specificata una condizione che Abilita una funzionalità durante l'installazione e Disabilita la funzionalità durante la disinstallazione.
-   Il file di chiave per il componente presenta un conteggio dei riferimenti precedente in **HKLM** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.
-   Il componente viene installato nella cartella di sistema e tutti i file nel componente hanno un conteggio dei riferimenti precedente in **HKLM** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.
-   Il Windows Installer non rimuove i file o le chiavi del registro di sistema protetti da [Protezione risorse di Windows](../wfp/windows-resource-protection-portal.md) (WRP). Per ulteriori informazioni, vedere [utilizzo di Windows Installer e protezione risorse di Windows](windows-resource-protection-on-windows-vista.md). In Windows Server 2003, Windows XP e Windows 2000, il programma di installazione non rimuove i file protetti da protezione file Windows (PAM). Se il file del percorso della chiave o la chiave del registro di sistema di un componente è protetta da WFP o WRP, il programma di installazione non rimuove il componente.
    > [!Note]  
    > Poiché Windows Installer non installa, aggiorna o rimuove alcuna risorsa protetta da WRP, è consigliabile non includere le risorse protette in un pacchetto di installazione. Usare invece solo i [meccanismi di sostituzione delle risorse supportati](../wfp/supported-file-replacement-mechanisms.md) descritti nella sezione [Protezione risorse di Windows](../wfp/windows-resource-protection-portal.md) .

     

 

 
