---
description: ICE25 convalida che un file .msi soddisfa tutte le dipendenze e le esclusioni interne del modulo unione.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2715ce629ad22b872b8d38d0c6848236b9f1af9378a0a652b702e7b72cbd7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528951"
---
# <a name="ice25"></a>ICE25

ICE25 convalida che un file .msi soddisfa tutte le [](merge-modules.md) dipendenze e le esclusioni interne del modulo unione. ICE convalida quanto segue:

-   Che tutte le dipendenze del modulo unione indicate nella tabella [ModuleDependency](moduledependency-table.md) del file .msi siano soddisfatte da almeno un modulo unione elencato nella [tabella ModuleSignature](modulesignature-table.md).
-   Nessuno dei moduli unione esclusi nella tabella [ModuleExclusion](moduleexclusion-table.md) è incompatibile con i moduli unione elencati nella [tabella ModuleSignature](modulesignature-table.md).

## <a name="result"></a>Risultato

ICE25 invia un messaggio di errore se .msi file è stato precedentemente unito a un modulo unione incompatibile o se non è stato unito a un modulo unione necessario.

## <a name="example"></a>Esempio

ICE25 pubblica gli errori seguenti per l'esempio illustrato.

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[Tabella ModuleSignature](modulesignature-table.md)



| ModuleID | Linguaggio | Versione |
|----------|----------|---------|
| Modulo A  | 0        | 1.0     |
| ModuloB  | 1033     | 1.0     |



 

[Tabella ModuleDependency](moduledependency-table.md)



| ModuleID | ModuleLanguage | Id obbligatorio | RequiredLanguage | RequiredVersion |
|----------|----------------|------------|------------------|-----------------|
| Modulo A  | 0              | ModuleX    | 0                | 2.0             |



 

[Tabella ModuleExclusion](moduleexclusion-table.md)



| ModuleID | ModuleLanguage | ExcludedID | Lingua esclusa | ExcludedMinVersion | ExcludedMaxVersion |
|----------|----------------|------------|------------------|--------------------|--------------------|
| Modulo A  | 0              | ModuloB    | 1033             |                    |                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



