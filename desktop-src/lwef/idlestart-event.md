---
title: IdleStart Event
description: IdleStart Event
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81458d4c88bc5db4ae4231ecb4ca47f456700917f42d6ccdfe5a6013bc288849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716051"
---
# <a name="idlestart-event"></a>IdleStart Event

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando il server imposta un carattere sullo **stato idling.**

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent*** \_ IdleStart* *  **(ByVal** *CharacterID***)**



| Parte          | Descrizione                                         |
|---------------|-----------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere di identificazione come stringa. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Il server invia questo evento a tutti i client del carattere.

### <a name="see-also"></a>Vedere anche

[**IdleComplete - evento**](idlecomplete-event.md)


 

 




