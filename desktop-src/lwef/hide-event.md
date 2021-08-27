---
title: Nascondi evento
description: Nascondi evento
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02974d1d66a22eab24c93fc5c9d29b9c2d0e604082fef9f4f0583ebcf7354576
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062061"
---
# <a name="hide-event"></a>Nascondi evento

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando un carattere è nascosto.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent*** \_ Hide(* *  **ByVal** *CharacterID,* **ByVal** *Cause***)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere nascosto come stringa.                                                                                                                                                                                                                                                                                                                                                               |
| *Causa*       | Restituisce un valore che indica l'elemento che ha causato la nascondere del carattere. 1 L'utente ha nascosto il carattere selezionando il comando nel menu a comparsa dell'icona della barra delle applicazioni del carattere o usando l'input vocale.<br/> 3 L'applicazione client ha nascosto il carattere.<br/> 5 Un'altra applicazione client ha nascosto il carattere.<br/> 7 L'utente ha nascosto il carattere selezionando il comando nel menu a comparsa del carattere.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Il server invia questo evento a tutti i client del carattere. Per eseguire una query sullo stato corrente del carattere, usare la [**proprietà Visible.**](visible-property.md)

### <a name="see-also"></a>Vedere anche

[**Mostra evento**](show-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





