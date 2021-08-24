---
title: Proprietà VisibilityCause
description: Proprietà VisibilityCause
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1e90b77dfdfae364761254676d0867a43aebacf516d4f2adad2973700d7e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398791"
---
# <a name="visibilitycause-property"></a>Proprietà VisibilityCause

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore intero che specifica l'elemento che ha causato lo stato visibile del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*Agent*. **Characters("**_CharacterID_*_"). VisibilityCause_*



| Valore | Descrizione                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| 0     | Il carattere non è stato visualizzato.                                                                            |
| 1     | L'utente ha nascosto il carattere usando il comando nel menu a comparsa dell'icona della barra delle applicazioni del carattere o usando l'input vocale. |
| 2     | L'utente ha mostrato il carattere.                                                                               |
| 3     | L'applicazione ha nascosto il carattere.                                                                          |
| 4     | L'applicazione ha mostrato il carattere .                                                                       |
| 5     | Un'altra applicazione client ha nascosto il carattere.                                                                |
| 6     | Il carattere è stato mostrato da un'altra applicazione client.                                                             |
| 7     | L'utente ha nascosto il carattere usando il comando nel menu a comparsa del carattere.                                 |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usare questa proprietà per determinare cosa ha causato lo spostamento del carattere quando più applicazioni condividono (ha caricato) lo stesso carattere. Questi valori sono uguali a quelli restituiti dagli [**eventi Show**](show-event.md) [**e Hide.**](hide-event.md)

## <a name="see-also"></a>Vedere anche

[**Hide event**](hide-event.md), [**Show event,**](show-event.md) [**Hide method**](hide-method.md), Show [**method**](show-method.md)


 

 




