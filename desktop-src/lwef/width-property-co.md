---
title: Proprietà Width (oggetto characters)
description: Width (proprietà)
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a37a29bd8f50231bd44b6529a0c1ce13c0256d3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047714"
---
# <a name="width-property-characters-object"></a>Proprietà Width (oggetto characters)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta la larghezza del frame per il carattere specificato.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agente ***. Caratteri ("**_CharacterID_*_")._ *  \[ =  *Valore* larghezza\]



| Parte    | Descrizione                                                |
|---------|------------------------------------------------------------|
| *value* | Valore long integer che specifica la larghezza del frame del carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà [**Width**](width-property.md) è sempre espressa in pixel. L'impostazione di questa proprietà si applica a tutti i client del carattere.

Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor dei caratteri di Microsoft Agent.

 

 




