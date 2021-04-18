---
title: Proprietà Visible (oggetto characters)
description: Visible (proprietà)
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a994fd59e5eaaebcaabbd9257b860fa4e27a09b4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300727"
---
# <a name="visible-property-characters-object"></a>Proprietà Visible (oggetto characters)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore booleano che indica se il carattere è visibile.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi** 
</dt> <dd>

*agente ***. Caratteri (**"* CharacterID *" * *). Visibile**



| Valore | Descrizione                            |
|-------|----------------------------------------|
| True  | Viene visualizzato il carattere.            |
| Falso | Il carattere è nascosto (non visibile). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà indica se viene visualizzato il frame del carattere. Non significa necessariamente che sia presente un'immagine sullo schermo. Questa proprietà, ad esempio, restituisce **true** anche quando il carattere è posizionato all'esterno dell'area di visualizzazione visibile o quando il frame di caratteri corrente non contiene immagini. L'impostazione di questa proprietà si applica a tutti i client del carattere.

Questa proprietà è di sola lettura. Per rendere un carattere visibile o nascosto, utilizzare i metodi [**Mostra**](show-method.md) o [**Nascondi**](https://www.bing.com/search?q=**Hide**) .

 

 




