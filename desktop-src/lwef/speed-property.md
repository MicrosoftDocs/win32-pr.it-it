---
title: Proprietà Speed
description: Proprietà Speed
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24738ac17d7efac45f2aefe7e4beb5ec018915a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298061"
---
# <a name="speed-property"></a>Proprietà Speed

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore long integer che specifica la velocità corrente dell'output vocale del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). Velocità**

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà restituisce l'impostazione della velocità di output in lettura corrente per il carattere. Per i caratteri che usano l'output TTS, la proprietà restituisce l'impostazione di output TTS effettivo per il carattere. Se TTS non è abilitato o il carattere non supporta l'output TTS, l'impostazione riflette l'impostazione utente per la velocità di output.

Anche se l'applicazione non è in grado di scrivere questo valore, è possibile includere tag **SPD** (Speed) nel testo di output che accelererà temporaneamente l'output per una determinata espressione. Tuttavia, l'uso del tag **SPD** per modificare l'output parlato del carattere non influisce sull'impostazione della proprietà **Speed** . Per altre informazioni, vedere [tag di output vocale](microsoft-agent-speech-output-tags.md).

 

 




