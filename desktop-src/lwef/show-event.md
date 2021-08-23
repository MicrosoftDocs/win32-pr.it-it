---
title: Mostra evento
description: Mostra evento
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b126c7726f8b8ed3ce1e83162cf41ad3223700630167448ff8a7655817a0604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975741"
---
# <a name="show-event"></a>Mostra evento

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando viene visualizzato un carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent*** \_ Show (ByVal* *  *CharacterID,* **ByVal** *Cause***)**



| Parte          | Descrizione                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere visualizzato come stringa.                                                                                                                                                                                                                          |
| *Causa*       | Restituisce un valore che indica la causa della visualizzazione del carattere. 2 L'utente ha mostrato il carattere (usando il menu o il comando vocale).<br/> 4 L'applicazione client ha mostrato il carattere.<br/> 6 Un'altra applicazione client ha mostrato il carattere.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Il server invia questo evento a tutti i client del carattere. Per eseguire una query sullo stato corrente del carattere, usare la [**proprietà Visible.**](visible-property.md)

### <a name="see-also"></a>Vedere anche

[**Nascondere l'evento**](hide-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





