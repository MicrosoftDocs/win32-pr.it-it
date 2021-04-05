---
title: Proprietà MoveCause
description: Proprietà MoveCause
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7f91d068befa2b919c04818c46dbc1a48faa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856210"
---
# <a name="movecause-property"></a>Proprietà MoveCause

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore intero che specifica la causa dell'ultima spostamento del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente*. **Caratteri ("***CharacterID***"). MoveCause**



| Valore | Descrizione                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| 0     | Il carattere non è stato spostato.                                                          |
| 1     | L'utente ha spostato il carattere.                                                              |
| 2     | L'applicazione ha spostato il carattere.                                                      |
| 3     | Un'altra applicazione client ha spostato il carattere.                                            |
| 4     | Il Server Agent ha spostato il carattere per mantenerlo sullo schermo dopo una modifica della risoluzione dello schermo. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usare questa proprietà per determinare la causa dello spostamento del carattere, quando più di un'applicazione condivide (ha caricato) lo stesso carattere. Questi valori corrispondono a quelli restituiti dall'evento [**Move**](move-event.md) .

## <a name="see-also"></a>Vedere anche

[**Evento Move**](move-event.md), [ **metodo MoveTo**](moveto-method.md)


 

 




