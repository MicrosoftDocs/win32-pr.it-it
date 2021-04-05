---
description: La tabella delle proprietà contiene i nomi e i valori delle proprietà per tutte le proprietà definite nell'installazione. Le proprietà con valori null non sono presenti nella tabella.
ms.assetid: 1f4215b2-dc71-4e6e-bc2e-3b43316806b9
title: Tabella delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612ab63aa36de6cf91ec8176eefec84cef591c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756482"
---
# <a name="property-table"></a>Tabella delle proprietà

La tabella delle proprietà contiene i nomi e i valori delle proprietà per tutte le proprietà definite nell'installazione. Le proprietà con valori null non sono presenti nella tabella.

La tabella delle proprietà contiene le colonne seguenti.



| Colonna   | Tipo                         | Chiave | Nullable |
|----------|------------------------------|-----|----------|
| Proprietà | [Identificatore](identifier.md) | S   | N        |
| Valore    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà
</dt> <dd>

Il nome di una proprietà. Vedere [Proprietà](properties.md).

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Valore stringa localizzabile per la proprietà. Non può mai essere null o una stringa vuota.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che non è possibile utilizzare la tabella delle proprietà per impostare una proprietà sul valore di un'altra proprietà. Il programma di installazione non esegue alcuna operazione sulla stringa di testo immessa nella colonna valore prima di impostare la proprietà nella colonna proprietà. Se FirstProperty viene immesso nella colonna proprietà e \[ SecondProperty \] nella colonna valore, il valore di FirstProperty viene impostato sulla stringa di testo " \[ SecondProperty \] " e non sul valore della proprietà SecondProperty. Questa operazione è necessaria per evitare la creazione di riferimenti circolari nella tabella delle proprietà. È invece possibile impostare una proprietà su un'altra usando un' [azione personalizzata di tipo 51](custom-action-type-51.md).

Si noti che la proprietà [**AdminProperties**](adminproperties.md) può essere utilizzata per eseguire l'override dei valori nella tabella delle proprietà durante un' [installazione amministrativa](administrative-installation.md).

Non usare le proprietà per le password o altre informazioni che devono rimanere sicure. Il programma di installazione può scrivere il valore di una proprietà creata nella tabella delle proprietà o creato in fase di esecuzione in un log o nel registro di sistema.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE05](ice05.md)  
[ICE06](ice06.md)  
[ICE16](ice16.md)  
[ICE24](ice24.md)  
[ICE31](ice31.md)  
[ICE34](ice34.md)  
[ICE36](ice36.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE48](ice48.md)  
[ICE52](ice52.md)  
[ICE61](ice61.md)  
[ICE73](ice73.md)  
[ICE74](ice74.md)  
[ICE80](ice80.md)  
[ICE87](ice87.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
[ICE99](ice99.md)  
</dl>

 

 



