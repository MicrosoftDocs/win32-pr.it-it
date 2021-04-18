---
title: Proprietà SoundEffects
description: Proprietà SoundEffects
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca45d373d39d479c62149a131f2a6678e5ecdf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298107"
---
# <a name="soundeffects-property"></a>Proprietà SoundEffects

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore booleano che indica se gli effetti audio (. WAV) i file configurati come parte delle azioni di un carattere vengono riprodotti.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente * * *. AudioOutput.SoundEffects**



| Valore     | Descrizione                          |
|-----------|--------------------------------------|
| **True**  | Gli effetti audio del carattere sono abilitati. |
| **False** | L'effetto audio carattere è disabilitato. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà riflette l'opzione Play Character Sound Effects nella pagina output della finestra delle proprietà dell'agente (Opzioni carattere avanzate). Quando la proprietà **SoundEffects** restituisce **true**, verranno riprodotti gli effetti audio inclusi nella definizione di un carattere. Se è **false**, gli effetti audio non verranno riprodotti. L'impostazione della proprietà ha effetto su tutti i caratteri ed è di sola lettura. il valore della proprietà può essere impostato solo dall'utente.

## <a name="see-also"></a>Vedere anche

[**Evento AgentPropertyChange**](agentpropertychange-event.md)


 

 




