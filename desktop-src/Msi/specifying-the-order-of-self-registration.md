---
description: Si noti che non è possibile specificare l'ordine in cui il programma di installazione registra o annulla la registrazione delle DLL autoregistrate usando le azioni SelfRegModules e SelfUnRegModules.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Specifica dell'ordine di registrazione automatica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb26fbebad3167fbea95679a1ea7a29c28946ae6fa2dd2b014be6ade986e28f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039681"
---
# <a name="specifying-the-order-of-self-registration"></a>Specifica dell'ordine di registrazione automatica

Si noti che non è possibile specificare l'ordine in cui il programma di installazione registra o annulla la registrazione delle DLL autoregistrate usando le azioni [SelfRegModules](selfregmodules-action.md) e [SelfUnRegModules.](selfunregmodules-action.md) Queste azioni registrano tutti i moduli elencati nella [tabella SelfReg](selfreg-table.md). Il programma di installazione non esegue la registrazione .exe file.

Per specificare l'ordine in cui il programma di installazione registra o annulla la registrazione dei moduli, è necessario usare due [azioni personalizzate](custom-actions.md) per ogni modulo. Un'azione personalizzata per DllRegisterServer e una seconda per DllUnregisterServer. Queste azioni personalizzate devono quindi essere scritte nella tabella [InstallExecuteSequence](installexecutesequence-table.md) nel punto della sequenza in cui la DLL deve essere registrata o annullata.

L'esempio seguente illustra come creare il database per pianificare la registrazione automatica di una DLL in un determinato punto della sequenza di azioni.

[Tabella file](file-table.md) (parziale)



| File  | Componente\_ | FileName  | Sequenza |
|-------|-------------|-----------|----------|
| mydll | myComponent | Mydll.dll | 13       |



 

[Tabella dei componenti](component-table.md) (parziale)



| Componente   | Componentid | Directory\_ | KeyPath |
|-------------|-------------|-------------|---------|
| myComponent | {*a GUID*}  | myFolder    | mydll   |



 

[Tabella directory](directory-table.md)



| Directory | Padre \_ della directory | DefaultDir          |
|-----------|-------------------|---------------------|
| Targetdir |                   | SourceDir           |
| myFolder  | Targetdir         | Cartella \| myFolder My Folder |



 

[Tabella CustomAction](customaction-table.md)



| Azione     | Tipo | Source (Sorgente)   | Destinazione                                     |
|------------|------|----------|--------------------------------------------|
| mydllREG   | 3170 | myFolder | " \[ SystemFolder \] msiexec" /y " \[ \# mydll \] " |
| mydllUNREG | 3170 | myFolder | " \[ SystemFolder \] msiexec" /z " \[ \# mydll \] " |



 

[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)



| Azione           | Condition         | Sequenza |
|------------------|-------------------|----------|
| SelfUnregModules |                   | 2200     |
| mydllUNREG       | $myComponent=2    | 2201     |
| RemoveFiles      |                   | 3500     |
| InstallFiles     |                   | 4000     |
| SelfRegModules   |                   | 6500     |
| mydllREG         | $myComponent>2 | 6501     |



 

 

 



