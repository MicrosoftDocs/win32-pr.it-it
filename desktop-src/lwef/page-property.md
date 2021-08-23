---
title: Proprietà pagina
description: Proprietà pagina
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ca14a4f68c326d1b231aa106450fefc7607857576f817ffaa255fa27f2249b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601010"
---
# <a name="page-property"></a>Proprietà pagina

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta la pagina visualizzata nella finestra delle proprietà di Microsoft Agent.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agent***. PropertySheet.Page* *  \[  =  *stringa*\]



| Parte     | Descrizione                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Espressione stringa con uno dei valori seguenti. **"Voce"** Visualizza la pagina Input vocale.<br/> **"Output"** Visualizza la pagina Output.<br/> **"Copyright"** Visualizza la pagina Copyright.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se non è installato alcun motore di riconoscimento vocale, **l'impostazione di Pagina** **su "Voce"** non ha alcun effetto. Inoltre, la proprietà Visible della **finestra** deve essere impostata su **True** perché l'utente veda la pagina.

> [!Note]  
> L'utente può eseguire l'override di questa proprietà.

 

 

 





