---
title: Proprietà Visible (oggetto Command)
description: Visible (proprietà)
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feaa6603812bf0938e6639021eb0f8660382af37
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300726"
---
# <a name="visible-property-command-object"></a>Proprietà Visible (oggetto Command)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che indica se il [**comando**](/windows/desktop/lwef/the-command-object) è visibile nel menu popup del carattere.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agente ***. Caratteri (**"* CharacterID *"**). Comandi (**"* nome *" * *).* *  \[  =  *Valore booleano* visibile\]



| Parte      | Descrizione                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se la didascalia del [**comando**](/windows/desktop/lwef/the-command-object)viene visualizzata nel menu di scelta rapida del carattere.<br/> **True** (impostazione predefinita) viene visualizzata la didascalia.<br/> **False** La didascalia non viene visualizzata.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Impostare questa proprietà su **false** se si desidera includere l'input vocale per le interfacce personali senza visualizzarlo nel menu a comparsa per il carattere. Se si imposta la proprietà [**Caption**](caption-property.md) di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) sulla stringa vuota (""), il testo della didascalia non verrà visualizzato nel menu di scelta rapida (ad esempio, come riga vuota), indipendentemente dalla relativa impostazione della proprietà [**Visible**](visible-property.md) .

L'impostazione della proprietà [**Visible**](visible-property.md) della raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) padre di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) non influisce sull'impostazione della proprietà **Visible** del **comando**.

 

