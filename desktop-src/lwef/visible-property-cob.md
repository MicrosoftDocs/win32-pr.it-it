---
title: Proprietà Visible (oggetto Characters)
description: Informazioni sulla proprietà Visible dell'oggetto Characters, che restituisce un valore booleano che indica se il carattere è visibile.
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78cce163e7ddfa8af3bf9198cd08bbb42be127745ed419a2f487aac6a1b7f287
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882232"
---
# <a name="visible-property-characters-object"></a>Proprietà Visible (oggetto Characters)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore booleano che indica se il carattere è visibile.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Visibile**



| Valore | Descrizione                            |
|-------|----------------------------------------|
| True  | Viene visualizzato il carattere .            |
| Falso | Il carattere è nascosto (non visibile). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà indica se il frame del carattere viene visualizzato. Non significa necessariamente che sia presente un'immagine sullo schermo. Ad esempio, questa proprietà restituisce **True** anche quando il carattere è posizionato fuori dall'area di visualizzazione visibile o quando la cornice del carattere corrente non contiene immagini. L'impostazione di questa proprietà si applica a tutti i client del carattere.

Questa proprietà è di sola lettura. Per rendere visibile o nascosto un carattere, usare i [**metodi Mostra**](show-method.md) [**o Nascondi.**](https://www.bing.com/search?q=**Hide**)

 

 




