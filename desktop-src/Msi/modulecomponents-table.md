---
description: La tabella ModuleComponents contiene un elenco dei componenti presenti nel modulo unione.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Tabella ModuleComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25216833022ada7592511091c6954222d8ebf354e732c95a54e8857948963541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926481"
---
# <a name="modulecomponents-table"></a>Tabella ModuleComponents

La tabella ModuleComponents contiene un elenco dei componenti presenti nel modulo unione.

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

Identificatore che fa riferimento a un componente nel modulo unione. La colonna Componente è una chiave esterna della [tabella Component](component-table.md). La voce nella colonna Componente deve seguire la convenzione di denominazione in [Denominazione delle chiavi primarie nei database del modulo unione](naming-primary-keys-in-merge-module-databases.md).

</dd> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>Moduleid
</dt> <dd>

Identificatore per il modulo unione. Si tratta di una chiave esterna per [la tabella ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Lingua
</dt> <dd>

L'identificatore della lingua descrive la lingua predefinita per il modulo unione. L'identificatore di lingua è in formato decimale, ad esempio l'inglese degli Stati Uniti è 1033. Chiave esterna per la [tabella ModuleSignature](modulesignature-table.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Le trasformazioni del linguaggio devono essere in grado di aggiornare questa tabella se il modulo unione supporta più lingue.

 

 



