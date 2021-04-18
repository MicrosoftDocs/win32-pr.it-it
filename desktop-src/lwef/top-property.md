---
title: Proprietà Top (oggetto characters)
description: Top (proprietà)
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef724c7052ad1d9ba5cb51ea46ccd7647723ed32
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300804"
---
# <a name="top-property-characters-object"></a>Proprietà Top (oggetto characters)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il bordo superiore del frame del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("**_CharacterID_*_")._ *  \[  =  *Valore* superiore\]



| Parte    | Descrizione                                             |
|---------|---------------------------------------------------------|
| *value* | Valore long integer che specifica il bordo superiore del carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La proprietà **Top** è sempre espressa in pixel, in relazione all'origine dello schermo (in alto a sinistra). L'impostazione di questa proprietà si applica a tutti i client del carattere.

Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor dei caratteri di Microsoft Agent.

Usare il metodo [**MoveTo**](moveto-method.md) per modificare la posizione del carattere.

## <a name="see-also"></a>Vedere anche

[**Proprietà Left**](left-property.md), [ **metodo MoveTo**](moveto-method.md)


 

 




