---
title: Proprietà Visible (oggetto Commands)
description: Informazioni sulla proprietà Visible dell'oggetto Commands, che determina se la didascalia della raccolta Commands viene visualizzata nel menu a comparsa del carattere.
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ea780ed5f19dbe732b18de741f9d7ee376df67
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396256"
---
# <a name="visible-property-commands-object"></a>Proprietà Visible (oggetto Commands)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

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

Perché la didascalia venga visualizzata nel menu a comparsa del carattere quando l'applicazione non è il client attivo per l'input, questa proprietà deve essere impostata su **True** e la proprietà [**Caption**](caption-property.md) deve essere impostata per la raccolta Commands. Inoltre, questa proprietà deve essere impostata su **True** perché i comandi nella raccolta vengano visualizzati nel menu a comparsa quando l'applicazione è attiva per l'input.

 

