---
title: Proprietà attiva
description: Proprietà attiva
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fe5fea7d94586c9f9d5c12b3a3b11ffbd7c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221424"
---
# <a name="active-property"></a>Proprietà attiva

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore che indica se l'applicazione è il client attivo del carattere e se il carattere è in primo piano.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente. ***Caratteri * * * * ("*** CharacterID * * *").* *  \[  =  *Stato* attivo\]



| Parte    | Descrizione                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *state* | Espressione Integer che specifica lo stato dell'applicazione client. 0 non è il client attivo.<br/> 1 il client attivo. <br/> 2 il client attivo di input. (Il carattere in primo piano).<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando più applicazioni client condividono lo stesso carattere, il client attivo del carattere riceve l'input del mouse, ad esempio gli eventi [**Click**](click-event.md) o [DragStart](dragstart-event.md) del controllo Microsoft Agent. Analogamente, quando vengono visualizzati più caratteri, il client attivo del carattere superiore (noto anche come client attivo di input) riceve gli eventi di comando.

È possibile usare il metodo [**Activate**](activate-method.md)per impostare se l'applicazione è il client attivo del carattere o per rendere l'applicazione il client attivo di input (che rende anche il carattere in primo piano).

## <a name="see-also"></a>Vedere anche

[Attivare il metodo * * * *](activate-method.md)


 

 





