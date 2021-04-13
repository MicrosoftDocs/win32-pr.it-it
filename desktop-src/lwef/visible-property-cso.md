---
title: Proprietà Visible (oggetto Commands)
description: Visible (proprietà)
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaba059a375c23569195ddaea82e6d03cb943ec
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400164"
---
# <a name="visible-property-commands-object"></a>Proprietà Visible (oggetto Commands)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che determina se la didascalia della raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) viene visualizzata nel menu di scelta rapida del carattere.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agente ***. Caratteri (**"* CharacterID *" * *).* *  \[  =  *Booleano* Commands. Visible\]



| Parte      | Descrizione                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) viene visualizzato nel menu di scelta rapida del carattere. <br/> Valore **true** Viene visualizzata la didascalia.<br/> **False** La didascalia non viene visualizzata.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Per visualizzare la didascalia nel menu di scelta rapida del carattere quando l'applicazione non è il client input-attivo, questa proprietà deve essere impostata su **true** e la proprietà [**Caption**](caption-property.md) impostata per la raccolta di comandi. Inoltre, questa proprietà deve essere impostata su **true** per visualizzare i comandi della raccolta nel menu a comparsa quando l'applicazione è di input-attivo.

 

