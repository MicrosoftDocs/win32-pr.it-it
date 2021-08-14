---
title: Proprietà MoveCause
description: Proprietà MoveCause
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa797338e64edfd67ae2347f2983df624464df923a64883e3adc5143671b15dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883832"
---
# <a name="movecause-property"></a>Proprietà MoveCause

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore intero che specifica la causa dell'ultimo spostamento del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*Agent*. **Characters("**_CharacterID_*_"). MoveCause_*



| Valore | Descrizione                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| 0     | Il carattere non è stato spostato.                                                          |
| 1     | L'utente ha spostato il carattere.                                                              |
| 2     | L'applicazione ha spostato il carattere.                                                      |
| 3     | Un'altra applicazione client ha spostato il carattere.                                            |
| 4     | Il server Agent ha spostato il carattere per mantenerlo sullo schermo dopo una modifica della risoluzione dello schermo. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usare questa proprietà per determinare cosa ha causato lo spostamento del carattere, quando più applicazioni condividono (ha caricato) lo stesso carattere. Questi valori sono uguali a quelli restituiti [**dall'evento Move.**](move-event.md)

## <a name="see-also"></a>Vedere anche

[**Evento Move**](move-event.md), [ **metodo MoveTo**](moveto-method.md)


 

 




