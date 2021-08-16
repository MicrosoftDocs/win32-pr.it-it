---
title: Proprietà Description (funzionalità dell'Windows legacy)
description: Proprietà Description
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7ff293af98303fa0dab97aca76ed169123ea229c1fc70c156ef2c099472157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751993"
---
# <a name="description-property-legacy-windows-environment-features"></a>Proprietà Description (funzionalità dell'Windows legacy)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta una stringa che specifica la descrizione per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent*. **Characters("**_CharacterID_*_"). Stringa di_* \[  =  *descrizione*\]



| Parte     | Descrizione                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| *string* | Valore stringa corrispondente alla descrizione del carattere (nell'impostazione della lingua corrente). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La descrizione di **un** carattere può dipendere dall'impostazione **LanguageID del** carattere. Il nome di un carattere in una lingua può essere diverso o usare caratteri diversi rispetto a in un'altra. La descrizione predefinita **del** carattere per una lingua specifica viene definita quando il carattere viene compilato con Microsoft Agent Character Editor.

> [!Note]  
> **L'impostazione** della proprietà Description è facoltativa e non può essere specificata per tutti i caratteri.

 

 

 




