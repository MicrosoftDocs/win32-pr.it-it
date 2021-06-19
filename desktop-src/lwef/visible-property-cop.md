---
title: Proprietà Visible (oggetto Command)
description: Informazioni sulla proprietà Visible dell'oggetto Command, che restituisce o imposta se il comando è visibile nel menu a comparsa del carattere.
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4efec1ad8a97d6412a560a81836273b93ebf2b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396246"
---
# <a name="visible-property-command-object"></a>Proprietà Visible (oggetto Command)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un [**valore che**](/windows/desktop/lwef/the-command-object) indica se il comando è visibile nel menu a comparsa del carattere.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Commands(**"* name *"**). Valore* *  \[  =  *booleano visibile*\]



| Parte      | Descrizione                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se [**la**](/windows/desktop/lwef/the-command-object)didascalia del comando viene visualizzata nel menu a comparsa del carattere.<br/> **True** (impostazione predefinita) Viene visualizzata la didascalia.<br/> **False** La didascalia non viene visualizzata.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Impostare questa proprietà **su False** quando si vuole includere l'input vocale per le proprie interfacce senza che vengano visualizzate nel menu a comparsa per il carattere. Se si imposta la proprietà [**Caption**](caption-property.md) di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) sulla stringa vuota (""), il testo della didascalia non verrà visualizzato nel menu a comparsa ,ad esempio come riga vuota, indipendentemente dall'impostazione della proprietà [**Visible.**](visible-property.md)

[**L'impostazione**](visible-property.md) della proprietà [**Visible della raccolta Commands**](/windows/desktop/lwef/the-command-object) padre di un oggetto [**Command**](/windows/desktop/lwef/the-commands-collection-object) non influisce sull'impostazione della proprietà **Visible** di **Command.**

 

