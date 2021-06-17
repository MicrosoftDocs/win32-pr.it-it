---
title: Proprietà Caption (oggetto Command)
description: Informazioni sulla proprietà Caption dell'oggetto Command. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0eb41def3b183fe4185b9c66a9ca5cd172372fb
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262553"
---
# <a name="caption-property-command-object"></a>Proprietà Caption (oggetto Command)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Determina il testo visualizzato per [**un oggetto Command**](/windows/desktop/lwef/the-command-object) nel menu a comparsa del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Commands("_*_name_*_"). Stringa_ *  \[  =  *didascalia*\]



| Parte     | Descrizione                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| *string* | Espressione stringa che restituisce il testo visualizzato come didascalia per **il comando**. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Per specificare un tasto di scelta (mnemotico non inline) per **caption**, includere un carattere e commerciale (&) prima di tale carattere.

Se non si definisce **voiceCaption** per il comando, verrà usata l'impostazione **Didascalia.**

 

 
