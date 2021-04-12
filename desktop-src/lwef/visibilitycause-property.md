---
title: Proprietà VisibilityCause
description: Proprietà VisibilityCause
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6e21e2cda201f8d04837d2b10efc757b93f824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396055"
---
# <a name="visibilitycause-property"></a>Proprietà VisibilityCause

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore intero che specifica ciò che ha causato lo stato visibile del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente*. **Caratteri ("***CharacterID***"). VisibilityCause**



| Valore | Descrizione                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| 0     | Il carattere non è stato visualizzato.                                                                            |
| 1     | L'utente ha nascosto il carattere usando il comando nel menu di scelta rapida dell'icona della barra delle applicazioni del carattere o usando l'input vocale. |
| 2     | L'utente ha mostrato il carattere.                                                                               |
| 3     | L'applicazione ha nascosto il carattere.                                                                          |
| 4     | L'applicazione ha mostrato il carattere.                                                                       |
| 5     | Un'altra applicazione client ha nascosto il carattere.                                                                |
| 6     | Un'altra applicazione client ha mostrato il carattere.                                                             |
| 7     | L'utente ha nascosto il carattere usando il comando nel menu a comparsa del carattere.                                 |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usare questa proprietà per determinare cosa ha causato lo spostamento del carattere quando più di un'applicazione condivide (ha caricato) lo stesso carattere. Questi valori corrispondono a quelli restituiti dagli eventi [**show**](show-event.md) e [**Hide**](hide-event.md) .

## <a name="see-also"></a>Vedere anche

[**Nascondi evento**](hide-event.md), [**Mostra evento**](show-event.md), [**Nascondi metodo**](hide-method.md), [**Mostra metodo**](show-method.md)


 

 




