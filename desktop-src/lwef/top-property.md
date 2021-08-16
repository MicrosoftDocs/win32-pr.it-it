---
title: Proprietà Top (oggetto Characters)
description: Informazioni sulla proprietà Top (oggetto Characters). Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bdc753bc287e1289b2a75633081c7b325d698a7fbe92ba495cc93662485d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474479"
---
# <a name="top-property-characters-object"></a>Proprietà Top (oggetto Characters)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

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


 

 




