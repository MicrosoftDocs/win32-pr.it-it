---
description: Se una tabella nel modulo unione è elencata nella tabella ModuleIgnoreTable, non viene unita nel file .msi merge.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: Tabella ModuleIgnoreTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46337b74f6822b374314a9248f0377ec63359c6576a6ca1398a931d27e548138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042859"
---
# <a name="moduleignoretable-table"></a>Tabella ModuleIgnoreTable

Se una tabella nel modulo unione è elencata nella tabella ModuleIgnoreTable, non viene unita nel file .msi merge. Se la tabella esiste già nel file .msi, non viene modificata dal merge. Le tabelle in ModuleIgnoreTable possono pertanto contenere dati non più disponibili dopo l'unione.

La tabella ModuleIgnoreTable include le colonne seguenti.



| Colonna | Tipo                         | Chiave | Nullable |
|--------|------------------------------|-----|----------|
| Tabella  | [Identificatore](identifier.md) | S   | No       |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo
</dt> <dd>

Nome della tabella nel modulo unione che non deve essere unita nel file .msi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ridurre al minimo le dimensioni del file con estensione msm, è consigliabile che gli sviluppatori rimuovono le tabelle inutilizzate dai moduli destinati alla ridistribuzione anziché elencare queste tabelle nella tabella ModuleIgnoreTable.

 

 



