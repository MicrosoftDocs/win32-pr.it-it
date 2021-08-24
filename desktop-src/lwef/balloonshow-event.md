---
title: Evento BalloonShow
description: Evento BalloonShow
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10aa8ab2c556fdf603a3972033a7440041fef6a45f828115c649a8a42810eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726141"
---
# <a name="balloonshow-event"></a>Evento BalloonShow

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando viene visualizzato il fumetto di parole di un carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

  \_ **BalloonShow dell'agente secondario** **(ByVal** *CharacterID***)**



| Parte          | Descrizione                                                       |
|---------------|-------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere associato al fumetto della parola. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Il server invia questo evento solo ai client del carattere (applicazioni che hanno caricato il carattere) che usa il fumetto della parola.

### <a name="see-also"></a>Vedere anche

[**Evento BalloonHide**](balloonhide-event.md)


 

 




