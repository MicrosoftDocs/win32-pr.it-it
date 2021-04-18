---
description: Questo esempio consente al consumer del modulo di configurare in modo indipendente un controllo di modifica, l'attributo checksum e l'attributo compresso.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Esempio di componente configurabile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971b2a7c442acb96d7ba00a444c8c3a038c339f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308198"
---
# <a name="configurable-component-example"></a>Esempio di componente configurabile

In questo esempio, le tabelle ModuleConfiguration e ModuleSubstitution seguenti consentono al consumer del modulo di configurare in modo indipendente l'attributo password per un controllo di modifica, l'attributo checksum per un file e l'attributo compresso per lo stesso file.

[Tabella ModuleSubstitution](modulesubstitution-table.md)



| Tabella   | Riga           | Colonna     | valore                        |
|---------|---------------|------------|------------------------------|
| Control | Dialog1; Edit1 | Attributi | \[= Password\]                |
| File    | File1         | Attributi | \[= Checksum \] \[ = compresso\] |



 

[Tabella ModuleConfiguration](moduleconfiguration-table.md)



| Nome       | Formato   | Tipo | ContextData                              | DefaultValue | Attributi | DisplayName | Descrizione |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| Password   | Bit |      | 2097152; True = 2097152; False = 0             | 0            | 0          |             |             |
| Checksum   | Bit |      | 1024; Checksum = 1024; Nessun checksum = 0         | 0            | 0          |             |             |
| Compresso | Bit |      | 24576; Compressi = 16384; Non compresso = 8192 | 8192         | 0          |             |             |



 

 

 



