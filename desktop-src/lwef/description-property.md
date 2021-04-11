---
title: Proprietà Description (funzionalità legacy dell'ambiente Windows)
description: Proprietà Description
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4fb60b20a57f56a914c7e44ced957d91bf7085
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047696"
---
# <a name="description-property-legacy-windows-environment-features"></a>Proprietà Description (funzionalità legacy dell'ambiente Windows)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta una stringa che specifica la descrizione per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente*. **Caratteri ("**_CharacterID_*_")._* \[  =  *Stringa* di descrizione\]



| Parte     | Descrizione                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| *string* | Valore stringa corrispondente alla descrizione del carattere (nell'impostazione della lingua corrente). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

La **Descrizione** di un carattere può dipendere dall'impostazione **LanguageID** del carattere. Il nome di un carattere in una lingua può essere diverso o usare caratteri diversi rispetto a un altro. La **Descrizione** predefinita del carattere per una lingua specifica viene definita quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.

> [!Note]  
> L'impostazione della proprietà **Description** è facoltativa e non può essere specificata per tutti i caratteri.

 

 

 




