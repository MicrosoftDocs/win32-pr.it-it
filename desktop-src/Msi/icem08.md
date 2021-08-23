---
description: ICEM08 garantisce che un modulo non escludi un altro modulo da cui dipende.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f5d0076de382889e5fd3df8a03dddb51c6a73eb5a4f825068f6cd66ad24d07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811011"
---
# <a name="icem08"></a>ICEM08

ICEM08 garantisce che un modulo non escludi un altro modulo da cui dipende.

## <a name="result"></a>Risultato

ICEM08 invia un errore quando un modulo esclude un altro modulo da cui dipende.

## <a name="example"></a>Esempio

ICEM08 invia il messaggio di errore seguente per un modulo contenente le voci di database illustrate nell'esempio.

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[Tabella ModuleDependency](moduledependency-table.md)



| ModuleID             | ModuleLanguage | RequiredID           | RequiredLanguage | RequiredVersion |
|----------------------|----------------|----------------------|------------------|-----------------|
| ModuleA.<GUID> | 1033           | ModuleB.<GUID> | 1033             | 1.0             |



 

[Tabella ModuleExclusion](moduleexclusion-table.md)



| ModuleID             | ModuleLanguage | ExcludedID           | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| ModuleA.<GUID> | 1033           | ModuleB.<GUID> | 1033             |                    | 1.0                |



 

Per correggere l'errore, rimuovere la dipendenza o l'esclusione. Se ModuleB è una dipendenza (RequiredID) di ModuleA, non è possibile escluderla (come illustrato nella colonna ExludedID della tabella ModuleExclusion). Se è necessario escludere ModuleB, è necessario rimuovere la dipendenza di ModuleA da esso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul modulo di unione ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



