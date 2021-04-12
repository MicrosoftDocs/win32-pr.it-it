---
title: Evento BalloonShow
description: Evento BalloonShow
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de67318b02775619332fe60ea47fb27edb893c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396511"
---
# <a name="balloonshow-event"></a>Evento BalloonShow

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando viene visualizzato il fumetto di parole di un carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *Agent* \_ **BalloonShow** **(ByVal** *CharacterID * * *)**



| Parte          | Descrizione                                                       |
|---------------|-------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere associato alla parola Balloon. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Il server invia questo evento solo ai client del carattere (le applicazioni che hanno caricato il carattere) che utilizza la parola fumetto.

### <a name="see-also"></a>Vedere anche

[**Evento BalloonHide**](balloonhide-event.md)


 

 




