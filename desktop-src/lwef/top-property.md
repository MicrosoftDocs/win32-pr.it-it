---
title: Proprietà Top (oggetto Characters)
description: Informazioni sulla proprietà Top (oggetto Characters). Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a5e26d2ef578a98447d47eb2a3fae3613760a9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396346"
---
# <a name="top-property-characters-object"></a>Proprietà Top (oggetto Characters)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il bordo superiore del frame del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Primo_ *  \[  =  *valore*\]



| Parte    | Descrizione                                             |
|---------|---------------------------------------------------------|
| *value* | Valore Long Integer che specifica il bordo superiore del carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La **proprietà Top** è sempre espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra). L'impostazione di questa proprietà si applica a tutti i client del carattere.

Anche se il carattere viene visualizzato in una finestra di area irregolare, la posizione del carattere è basata sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor di caratteri di Microsoft Agent.

Usare il [**metodo MoveTo**](moveto-method.md) per modificare la posizione del carattere.

## <a name="see-also"></a>Vedere anche

[**Proprietà Left**](left-property.md), [ **metodo MoveTo**](moveto-method.md)


 

 




