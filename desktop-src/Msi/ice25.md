---
description: ICE25 verifica che un file con estensione msi soddisfi tutte le dipendenze ed esclusioni dei moduli di merge interni.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d966c4c374d6e61e30b44a41ad88bed8bf907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882938"
---
# <a name="ice25"></a>ICE25

ICE25 verifica che un file con estensione msi soddisfi tutte le dipendenze ed esclusioni dei [moduli di merge](merge-modules.md) interni. ICE convalida quanto segue:

-   Tutte le dipendenze del modulo merge indicate nella [tabella ModuleDependency](moduledependency-table.md) del file con estensione msi vengono soddisfatte da almeno un modulo merge elencato nella [tabella ModuleSignature](modulesignature-table.md).
-   Nessuno dei moduli unione esclusi nella [tabella ModuleExclusion](moduleexclusion-table.md) non è compatibile con i moduli unione elencati nella [tabella ModuleSignature](modulesignature-table.md).

## <a name="result"></a>Risultato

ICE25 Invia un messaggio di errore se il file con estensione msi è stato precedentemente Unito a un modulo merge non compatibile o se non è stato unito a un modulo Merge necessario.

## <a name="example"></a>Esempio

ICE25 invia gli errori seguenti per l'esempio illustrato.

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[Tabella ModuleSignature](modulesignature-table.md)



| ModuleID | Linguaggio | Versione |
|----------|----------|---------|
| Modulo a  | 0        | 1.0     |
| ModuleB  | 1033     | 1.0     |



 

[Tabella ModuleDependency](moduledependency-table.md)



| ModuleID | ModuleLanguage | RequiredID | RequiredLanguage | RequiredVersion |
|----------|----------------|------------|------------------|-----------------|
| Modulo a  | 0              | ModuleX    | 0                | 2.0             |



 

[Tabella ModuleExclusion](moduleexclusion-table.md)



| ModuleID | ModuleLanguage | ExcludedID | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------|----------------|------------|------------------|--------------------|--------------------|
| Modulo a  | 0              | ModuleB    | 1033             |                    |                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



