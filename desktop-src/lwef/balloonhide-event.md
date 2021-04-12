---
title: Evento BalloonHide
description: Evento BalloonHide
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062a82afcabb3597ca8c254e039c231b52033657
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221955"
---
# <a name="balloonhide-event"></a>Evento BalloonHide

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando il fumetto di parole di un carattere è nascosto.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *Agent* \_ **BalloonHide** **(ByVal** *CharacterID * * *)**



| Parte          | Descrizione                                                       |
|---------------|-------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere associato alla parola Balloon. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Il server invia questo evento solo ai client del carattere (le applicazioni che hanno caricato il carattere) che utilizza la parola fumetto.

### <a name="see-also"></a>Vedere anche

[**Evento BalloonShow**](balloonshow-event.md)


 

 




