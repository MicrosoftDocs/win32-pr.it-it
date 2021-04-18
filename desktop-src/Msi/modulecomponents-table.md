---
description: La tabella ModuleComponents contiene un elenco dei componenti trovati nel modulo merge.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Tabella ModuleComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea2f47418b0387c7fa9d289d156fb0369f53adf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316746"
---
# <a name="modulecomponents-table"></a>Tabella ModuleComponents

La tabella ModuleComponents contiene un elenco dei componenti trovati nel modulo merge.

La tabella ModuleComponents include le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| Componente | [Identificatore](identifier.md) | S   | N        |
| ModuleID  | [Identificatore](identifier.md) | S   | N        |
| Linguaggio  | [Integer](integer.md)       | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Componente
</dt> <dd>

Identificatore che fa riferimento a un componente nel modulo merge. La colonna Component è una chiave esterna della [tabella Component](component-table.md). La voce nella colonna componente deve seguire la convenzione di denominazione per la [denominazione delle chiavi primarie nei database del modulo merge](naming-primary-keys-in-merge-module-databases.md).

</dd> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Identificatore per il modulo unione. Si tratta di una chiave esterna per la [tabella ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Linguaggio
</dt> <dd>

L'identificatore della lingua descrive la lingua predefinita per il modulo unione. L'identificatore di lingua è in formato decimale, ad esempio l'inglese (Stati Uniti) è 1033. Chiave esterna per la [tabella ModuleSignature](modulesignature-table.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Le trasformazioni del linguaggio devono essere in grado di aggiornare questa tabella se il modulo merge supporta più lingue.

 

 



