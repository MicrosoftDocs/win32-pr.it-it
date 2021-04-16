---
description: Si noti che non è possibile specificare l'ordine in cui il programma di installazione registra o Annulla la registrazione delle dll autoregistrate usando le azioni SelfRegModules e SelfUnRegModules.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Specifica dell'ordine di registrazione automatica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d99587f6e6bdd8726f2cdc584fc2f399d81ae91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485380"
---
# <a name="specifying-the-order-of-self-registration"></a>Specifica dell'ordine di registrazione automatica

Si noti che non è possibile specificare l'ordine in cui il programma di installazione registra o Annulla la registrazione delle dll autoregistrate usando le azioni [SelfRegModules](selfregmodules-action.md) e [SelfUnRegModules](selfunregmodules-action.md) . Queste azioni registrano tutti i moduli elencati nella [tabella SelfReg](selfreg-table.md). Il programma di installazione non registra autonomamente i file exe.

Per specificare l'ordine in cui il programma di installazione registra o Annulla la registrazione dei moduli, è necessario usare due [azioni personalizzate](custom-actions.md) per ogni modulo. Un'azione personalizzata per DllRegisterServer e una seconda per DllUnregisterServer. Queste azioni personalizzate devono quindi essere create nella [tabella InstallExecuteSequence](installexecutesequence-table.md) in corrispondenza del punto della sequenza in cui deve essere registrata o annullata la registrazione della dll.

Nell'esempio seguente viene illustrato come creare il database per pianificare la registrazione automatica di una DLL in un determinato punto della sequenza di azione.

[Tabella file](file-table.md) (parziale)



| File  | Componente\_ | FileName  | Sequenza |
|-------|-------------|-----------|----------|
| mydll | myComponent | Mydll.dll | 13       |



 

[Tabella componenti](component-table.md) (parziale)



| Componente   | ComponentId | Directory\_ | KeyPath |
|-------------|-------------|-------------|---------|
| myComponent | {*GUID*}  | myFolder    | mydll   |



 

[Tabella directory](directory-table.md)



| Directory | \_Padre directory | DefaultDir          |
|-----------|-------------------|---------------------|
| TARGETDIR |                   | SourceDir           |
| myFolder  | TARGETDIR         | cartella \| My |



 

[Tabella CustomAction](customaction-table.md)



| Azione     | Tipo | Source (Sorgente)   | Destinazione                                     |
|------------|------|----------|--------------------------------------------|
| mydllREG   | 3170 | myFolder | " \[ SystemFolder \] msiexec"/y " \[ \# myDll \] " |
| mydllUNREG | 3170 | myFolder | " \[ SystemFolder \] msiexec"/z " \[ \# myDll \] " |



 

[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)



| Azione           | Condizione         | Sequenza |
|------------------|-------------------|----------|
| SelfUnregModules |                   | 2200     |
| mydllUNREG       | $myComponent = 2    | 2201     |
| RemoveFiles      |                   | 3500     |
| InstallFiles     |                   | 4000     |
| SelfRegModules   |                   | 6500     |
| mydllREG         | $myComponent>2 | 6501     |



 

 

 



