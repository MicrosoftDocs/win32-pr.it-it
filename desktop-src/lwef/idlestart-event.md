---
title: Evento IdleStart
description: Evento IdleStart
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706aafc13cb1639484539e3d08b305df217ecec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298218"
---
# <a name="idlestart-event"></a>Evento IdleStart

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando il server imposta un carattere sullo **stato di** inattivo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

Agente **secondario** ** * * \_ IdleStart* *  **(ByVal** *CharacterID * * *)**



| Parte          | Descrizione                                         |
|---------------|-----------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere minimo sotto forma di stringa. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Il server invia questo evento a tutti i client del carattere.

### <a name="see-also"></a>Vedere anche

[**Evento IdleComplete**](idlecomplete-event.md)


 

 




