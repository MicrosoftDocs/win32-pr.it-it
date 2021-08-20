---
title: Evento BalloonHide
description: Evento BalloonHide
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1d6137f1ade4827c9b42a0e2fed96db8ec763033515c7674ffb913d554d830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117694045"
---
# <a name="balloonhide-event"></a>Evento BalloonHide

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando il fumetto di parole di un carattere è nascosto.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

  \_ **BalloonHide dell'agente secondario** **(ByVal** *CharacterID***)**



| Parte          | Descrizione                                                       |
|---------------|-------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere associato al fumetto della parola. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Il server invia questo evento solo ai client del carattere (applicazioni che hanno caricato il carattere) che usa il fumetto della parola.

### <a name="see-also"></a>Vedere anche

[**Evento BalloonShow**](balloonshow-event.md)


 

 




