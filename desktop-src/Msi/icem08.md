---
description: ICEM08 garantisce che un modulo non escludi un altro modulo da cui dipende.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c953c40d29458613b0fc2027dd691adb672eb15
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884212"
---
# <a name="icem08"></a>ICEM08

ICEM08 garantisce che un modulo non escludi un altro modulo da cui dipende.

## <a name="result"></a>Risultato

ICEM08 invia un errore quando un modulo esclude un altro modulo da cui dipende.

## <a name="example"></a>Esempio

ICEM08 invia il messaggio di errore seguente per un modulo contenente le voci di database mostrate nell'esempio.

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[Tabella ModuleDependency](moduledependency-table.md)



| ModuleID             | ModuleLanguage | RequiredID           | RequiredLanguage | RequiredVersion |
|----------------------|----------------|----------------------|------------------|-----------------|
| ModuleA. &lt; GUID&gt; | 1033           | ModuleB. &lt; GUID&gt; | 1033             | 1.0             |



 

[Tabella ModuleExclusion](moduleexclusion-table.md)



| ModuleID             | ModuleLanguage | ExcludedID           | Lingua esclusa | ExcludedMinVersion | ExcludedMaxVersion |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| ModuleA. &lt; GUID&gt; | 1033           | ModuleB. &lt; GUID&gt; | 1033             |                    | 1.0                |



 

Per correggere l'errore, rimuovere la dipendenza o l'esclusione. Se ModuleB è una dipendenza (RequiredID) di ModuleA, non è possibile escluderla (come illustrato nella colonna ExludedID della tabella ModuleExclusion). Se è necessario escludere ModuleB, è necessario rimuovere la dipendenza di ModuleA da esso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE del modulo di merge](merge-module-ice-reference.md)
</dt> </dl>

 

 



