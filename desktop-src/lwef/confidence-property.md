---
title: Proprietà confidenza
description: Proprietà confidenza
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa004e5690c534b7467c293d26cdf60f327dcfb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398886"
---
# <a name="confidence-property"></a>Proprietà confidenza

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che indica se la **confidenza** del client viene visualizzata nel suggerimento di ascolto.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID ***"). Comandi ("*** Name ***")**. * ** *  \[  =  *numero* di confidenza\]



| Parte     | Descrizione                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| *Number* | Espressione numerica che restituisce un valore long integer che identifica il valore di confidenza per il [**comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se il valore di confidenza restituito della corrispondenza migliore (UserInput. Confidence) non supera il valore impostato per la proprietà **confidenza** , il testo fornito in [**ConfidenceText**](confidencetext-property.md) viene visualizzato nel suggerimento di ascolto.

 

 