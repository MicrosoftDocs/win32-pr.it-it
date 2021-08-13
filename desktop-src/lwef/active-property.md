---
title: Proprietà Active
description: Proprietà Active
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac75a83724c793f2a7aba01718d57e47b25a0dd6b467ca7797ad6f0e4ced018e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753170"
---
# <a name="active-property"></a>Proprietà Active

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore che indica se l'applicazione è il client attivo del carattere e se il carattere è in primo piano.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters****("**_CharacterID_*_"). Stato_ *  \[  =  *attivo*\]



| Parte    | Descrizione                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *state* | Espressione integer che specifica lo stato dell'applicazione client. 0 Non è il client attivo.<br/> 1 Il client attivo. <br/> 2 Client attivo di input. (Carattere in primo piano).<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando più applicazioni client condividono lo stesso carattere, il client attivo del carattere riceve l'input del mouse,ad esempio gli eventi [**Click**](click-event.md) o [DragStart](dragstart-event.md) del controllo Microsoft Agent. Analogamente, quando vengono visualizzati più caratteri, il client attivo del carattere più in alto (noto anche come client attivo di input) riceve gli eventi Command.

È possibile usare il [**metodo Activate**](activate-method.md)per impostare se l'applicazione è il client attivo del carattere o per impostare l'applicazione come client attivo di input (che rende anche il carattere più in alto).

## <a name="see-also"></a>Vedere anche

[Metodo Activate** **](activate-method.md)


 

 





