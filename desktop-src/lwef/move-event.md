---
title: Move Event
description: Move Event
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9938f79a0c23340c5ed34be52019afe5f9f3fa6caefb6920941cb17dc13c0fc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476349"
---
# <a name="move-event"></a>Move Event

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando un carattere viene spostato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent* \_ **Move (ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *Cause***)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere spostato.                                                                                                                                                                                                                                                                                                   |
| *X*           | Restituisce la coordinata x (in pixel) del bordo superiore della nuova posizione del frame di caratteri come intero.                                                                                                                                                                                                                                         |
| *S*           | Restituisce la coordinata y (in pixel) del bordo sinistro della nuova posizione del frame di caratteri come intero.                                                                                                                                                                                                                                        |
| *Causa*       | Restituisce un valore che indica ciò che ha causato lo spostamento del carattere. 1 L'utente ha trascinato il carattere.<br/> 2 L'applicazione client ha spostato il carattere.<br/> 3 Un'altra applicazione client ha spostato il carattere.<br/> 4 Il server Agent ha spostato il carattere per mantenerlo sullo schermo dopo una modifica della risoluzione dello schermo.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento si verifica quando l'utente o un'applicazione modifica la posizione del carattere. Le coordinate sono rilevanti per l'angolo superiore sinistro dello schermo. Questo evento viene inviato solo ai client del carattere (applicazioni che lo hanno caricato).

**Vedere anche**

[**Proprietà MoveCause**](movecause-property.md), [ **evento Size**](size-event.md)

 

 





