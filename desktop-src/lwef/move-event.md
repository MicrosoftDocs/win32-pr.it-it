---
title: Sposta evento
description: Sposta evento
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31facb1d57b807fb0322783a291b77ef5a7c1487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856209"
---
# <a name="move-event"></a>Sposta evento

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando viene spostato un carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

Spostamento dell'agente **secondario**  \_ **(ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *cause * * *)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere spostato.                                                                                                                                                                                                                                                                                                   |
| *X*           | Restituisce la coordinata x (in pixel) del bordo superiore della nuova posizione del frame di caratteri come valore integer.                                                                                                                                                                                                                                         |
| *S*           | Restituisce la coordinata y (in pixel) del bordo sinistro della nuova posizione del frame di caratteri come valore integer.                                                                                                                                                                                                                                        |
| *Causa*       | Restituisce un valore che indica la causa dello spostamento del carattere. 1 l'utente ha trascinato il carattere.<br/> 2 l'applicazione client ha spostato il carattere.<br/> 3 un'altra applicazione client ha spostato il carattere.<br/> 4 il server agente ha spostato il carattere per mantenerlo sullo schermo dopo una modifica della risoluzione dello schermo.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento si verifica quando l'utente o un'applicazione modifica la posizione del carattere. Le coordinate sono rilevanti per l'angolo superiore sinistro dello schermo. Questo evento viene inviato solo ai client del carattere, ovvero le applicazioni che hanno caricato il carattere.

**Vedere anche**

[**Proprietà MoveCause**](movecause-property.md), [ **evento size**](size-event.md)

 

 





