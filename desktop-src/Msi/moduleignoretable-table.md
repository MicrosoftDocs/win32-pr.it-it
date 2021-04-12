---
description: Se una tabella del modulo merge è elencata nella tabella ModuleIgnoreTable, non viene unita nel file con estensione msi.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: Tabella ModuleIgnoreTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b0191f616eced187411a148e40e0ae6575cca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233508"
---
# <a name="moduleignoretable-table"></a>Tabella ModuleIgnoreTable

Se una tabella del modulo merge è elencata nella tabella ModuleIgnoreTable, non viene unita nel file con estensione msi. Se la tabella esiste già nel file con estensione msi, non viene modificata dall'Unione. Le tabelle in ModuleIgnoreTable possono quindi contenere dati che non sono necessari dopo l'Unione.

La tabella ModuleIgnoreTable include le colonne seguenti.



| Colonna | Tipo                         | Chiave | Nullable |
|--------|------------------------------|-----|----------|
| Tabella  | [Identificatore](identifier.md) | S   | No       |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo
</dt> <dd>

Nome della tabella nel modulo merge che non deve essere sottoposta a merge nel file con estensione msi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ridurre al minimo le dimensioni del file con estensione MSM, è consigliabile che gli sviluppatori rimuovano le tabelle inutilizzate da moduli destinati alla ridistribuzione anziché elencare queste tabelle nella tabella ModuleIgnoreTable.

 

 



