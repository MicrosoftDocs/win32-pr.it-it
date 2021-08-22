---
title: Proprietà Visible (oggetto Commands)
description: Informazioni sulla proprietà Visible dell'oggetto Commands, che determina se la didascalia della raccolta Commands viene visualizzata nel menu a comparsa del carattere.
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c742733d06f0a4c7ae2d10c7fb97a20e735b59370c61efa5f7204003f1cd81bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975471"
---
# <a name="visible-property-commands-object"></a>Proprietà Visible (oggetto Commands)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che determina se la didascalia della raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) viene visualizzata nel menu a comparsa del carattere.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Valore booleano Commands.Visible* *  \[  =  \]



| Parte      | Descrizione                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se [**l'oggetto Commands**](/windows/desktop/lwef/the-commands-collection-object) viene visualizzato nel menu a comparsa del carattere. <br/> **True** Viene visualizzata la didascalia.<br/> **False** La didascalia non viene visualizzata.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Per visualizzare la didascalia nel menu a comparsa del carattere quando l'applicazione non è il client attivo per l'input, questa proprietà deve essere impostata su **True** e la proprietà [**Caption**](caption-property.md) impostata per la raccolta Commands. Inoltre, questa proprietà deve essere impostata su **True** perché i comandi nella raccolta vengano visualizzati nel menu a comparsa quando l'applicazione è attiva per l'input.

 

