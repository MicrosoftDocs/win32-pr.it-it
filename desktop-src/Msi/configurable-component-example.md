---
description: Questo esempio consente al consumer del modulo di configurare in modo indipendente un controllo di modifica, l'attributo checksum e l'attributo compresso.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Esempio di componente configurabile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ff3e1567a19afd50a0ae2035893c027398816b535d5edfb233e89021ea9e59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500741"
---
# <a name="configurable-component-example"></a>Esempio di componente configurabile

In questo esempio le tabelle ModuleConfiguration e ModuleSubstitution seguenti consentono al consumer del modulo di configurare in modo indipendente l'attributo Password per un controllo di modifica, l'attributo checksum per un file e l'attributo compresso per lo stesso file.

[Tabella ModuleSubstitution](modulesubstitution-table.md)



| Tabella   | Riga           | Colonna     | valore                        |
|---------|---------------|------------|------------------------------|
| Control | Dialog1; Modifica1 | Attributi | \[=Password\]                |
| File    | File1         | Attributi | \[=Checksum \] \[ =Compressed\] |



 

[Tabella ModuleConfiguration](moduleconfiguration-table.md)



| Nome       | Formato   | Tipo | ContextData                              | DefaultValue | Attributi | DisplayName | Descrizione |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| Password   | Campo di bit |      | 2097152; True=2097152; False=0             | 0            | 0          |             |             |
| Checksum   | Campo di bit |      | 1024; Checksum=1024; Nessun checksum=0         | 0            | 0          |             |             |
| Compresso | Campo di bit |      | 24576; Compressed=16384; Uncompressed=8192 | 8192         | 0          |             |             |



 

 

 



