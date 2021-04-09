---
title: Nascondi evento
description: Nascondi evento
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d396fb0985cd4c3c2e9647dfe0e7c9126ad9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856229"
---
# <a name="hide-event"></a>Nascondi evento

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando un carattere è nascosto.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *Agent * * * \_ Hide (* *  **ByVal** *CharacterID*, **ByVal** *cause * * *)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere nascosto sotto forma di stringa.                                                                                                                                                                                                                                                                                                                                                               |
| *Causa*       | Restituisce un valore che indica la causa del carattere da nascondere. 1 utente ha nascosto il carattere selezionando il comando nel menu a comparsa dell'icona della barra delle applicazioni del carattere o usando l'input vocale.<br/> 3 l'applicazione client ha nascosto il carattere.<br/> 5 un'altra applicazione client ha nascosto il carattere.<br/> 7 l'utente ha nascosto il carattere selezionando il comando nel menu a comparsa del carattere.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Il server invia questo evento a tutti i client del carattere. Per eseguire una query sullo stato corrente del carattere, utilizzare la proprietà [**Visible**](visible-property.md) .

### <a name="see-also"></a>Vedere anche

[**Mostra evento**](show-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





