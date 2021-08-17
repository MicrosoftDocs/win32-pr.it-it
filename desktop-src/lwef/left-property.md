---
title: Proprietà Left (oggetto Characters)
description: Informazioni sulla proprietà dell'oggetto Left Characters. Microsoft Agent è deprecato a Windows 7.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e546dc662dc535889eb6c3a476a54b839c5d9577a7e2ff525eeadf79f727fbf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105017"
---
# <a name="left-property-characters-object"></a>Proprietà Left (oggetto Characters)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il bordo sinistro del frame del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Valore_ *  \[  =  *a sinistra*\]



| Parte    | Descrizione                                                           |
|---------|-----------------------------------------------------------------------|
| *value* | Valore Long Integer che specifica il bordo sinistro del frame del carattere. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La **proprietà Left** è sempre espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra). L'impostazione di questa proprietà si applica a tutti i client del carattere.

Anche se il carattere viene visualizzato in una finestra di area irregolare, la posizione del carattere è basata sulle dimensioni esterne del frame di animazione rettangolare usato quando il carattere è stato compilato con l'editor di caratteri di Microsoft Agent.

 

 




