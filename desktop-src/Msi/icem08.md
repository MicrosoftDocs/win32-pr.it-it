---
description: ICEM08 garantisce che un modulo non escluda un altro modulo da cui dipende.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9767c6748f5a21d83bddb3b5fe93a0a8d7ea67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232447"
---
# <a name="icem08"></a>ICEM08

ICEM08 garantisce che un modulo non escluda un altro modulo da cui dipende.

## <a name="result"></a>Risultato

ICEM08 Invia un errore quando un modulo esclude un altro modulo da cui dipende.

## <a name="example"></a>Esempio

ICEM08 invia il messaggio di errore seguente per un modulo contenente le voci di database indicate nell'esempio.

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[Tabella ModuleDependency](moduledependency-table.md)



| ModuleID             | ModuleLanguage | RequiredID           | RequiredLanguage | RequiredVersion |
|----------------------|----------------|----------------------|------------------|-----------------|
| Modulo a.<GUID> | 1033           | ModuleB.<GUID> | 1033             | 1.0             |



 

[Tabella ModuleExclusion](moduleexclusion-table.md)



| ModuleID             | ModuleLanguage | ExcludedID           | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| Modulo a.<GUID> | 1033           | ModuleB.<GUID> | 1033             |                    | 1.0                |



 

Per correggere l'errore, rimuovere la dipendenza o l'esclusione. Se ModuleB è una dipendenza (RequiredID) di Modulea, non è possibile escluderla, come illustrato nella colonna ExludedID della tabella ModuleExclusion. Se è necessario escludere ModuleB, è necessario rimuovere la dipendenza di Modulea su di essa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 



