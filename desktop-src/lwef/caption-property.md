---
title: Proprietà Caption (oggetto Command)
description: Proprietà Caption
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0595444bd2e49ca0207c5a6a9fd459e919573958
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300798"
---
# <a name="caption-property-command-object"></a>Proprietà Caption (oggetto Command)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Determina il testo visualizzato per un [**comando**](/windows/desktop/lwef/the-command-object) nel menu di scelta rapida del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("**_CharacterID_*_"). Comandi ("_*_Name_*_"). Stringa didascalia_ *  \[  =  \]



| Parte     | Descrizione                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| *string* | Espressione stringa che restituisce il testo visualizzato come didascalia per il **comando**. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Per specificare un tasto di scelta (mnemonico) per la **didascalia**, includere un carattere e commerciale (&) prima di tale carattere.

Se non si definisce un **VoiceCaption** per il comando, verrà usata l'impostazione della **didascalia** .

 

 
