---
title: Proprietà Width (oggetto Characters)
description: Informazioni sulla proprietà Width dell'oggetto Characters, che restituisce o imposta la larghezza del frame per il carattere specificato.
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17f11412774fcf34e887a2f00479ab7d96369de
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395127"
---
# <a name="width-property-characters-object"></a>Proprietà Width (oggetto Characters)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta la larghezza del frame per il carattere specificato.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Valore_ *  \[ =  *larghezza*\]



| Parte    | Descrizione                                                |
|---------|------------------------------------------------------------|
| *value* | Valore Long Integer che specifica la larghezza del frame del carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La [**proprietà Width**](width-property.md) è sempre espressa in pixel. L'impostazione di questa proprietà si applica a tutti i client del carattere.

Anche se il carattere viene visualizzato in una finestra di area di forma irregolare, la posizione del carattere si basa sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor di caratteri di Microsoft Agent.

 

 




