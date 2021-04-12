---
title: Proprietà ConfidenceText
description: Proprietà ConfidenceText
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb30b5ac481b6011d3575ab99dbc389f426b085d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398949"
---
# <a name="confidencetext-property"></a>Proprietà ConfidenceText

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il **ConfidenceText** del client visualizzato nel suggerimento di ascolto.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

* Agent ***. Caratteri ("*** CharacterID ***"). Comandi ("*** nome ***")**.  \[ ConfidenceText  =  *stringa* di\]



| Parte     | Descrizione                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| *string* | Espressione stringa che restituisce il testo per **ConfidenceText** per il [**comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando il valore di confidenza restituito della corrispondenza migliore (UserInput. Confidence) non supera l'impostazione di [**attendibilità**](confidence-property.md) , nel server viene visualizzato il testo fornito in **ConfidenceText** nel suggerimento di ascolto.

 

 