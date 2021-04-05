---
title: Mostra evento
description: Mostra evento
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6964164e14c759a971e5ceeda542a5c27131663
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855770"
---
# <a name="show-event"></a>Mostra evento

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando viene visualizzato un carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *Agent * * * \_ Show (ByVal* *  *CharacterID*, **ByVal** *causare * * *)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere visualizzato sotto forma di stringa.                                                                                                                                                                                                                          |
| *Causa*       | Restituisce un valore che indica ciò che ha causato la visualizzazione del carattere. 2 l'utente ha visualizzato il carattere (usando il comando menu o Voice).<br/> 4 l'applicazione client ha mostrato il carattere.<br/> 6 un'altra applicazione client ha mostrato il carattere.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Il server invia questo evento a tutti i client del carattere. Per eseguire una query sullo stato corrente del carattere, utilizzare la proprietà [**Visible**](visible-property.md) .

### <a name="see-also"></a>Vedere anche

[**Nascondi evento**](hide-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





