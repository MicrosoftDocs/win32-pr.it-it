---
title: Proprietà Page
description: Proprietà Page
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c51f55e4d1e9c7d2d23713810412060d915c7af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395947"
---
# <a name="page-property"></a>Proprietà Page

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta la pagina visualizzata nella finestra delle proprietà di Microsoft Agent.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agente * * *.* *  \[  =  *Stringa* PropertySheet.Page\]



| Parte     | Descrizione                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Espressione stringa con uno dei valori seguenti. **"Sintesi vocale"** Visualizza la pagina di input vocale.<br/> **"Output"** Consente di visualizzare la pagina di output.<br/> **"Copyright"** Visualizza la pagina copyright.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se non è installato alcun motore vocale, l'impostazione della **pagina** su **"speech"** non ha alcun effetto. Inoltre, la proprietà **Visible** della finestra deve essere impostata su **true** in modo che l'utente visualizzi la pagina.

> [!Note]  
> L'utente può eseguire l'override di questa proprietà.

 

 

 





