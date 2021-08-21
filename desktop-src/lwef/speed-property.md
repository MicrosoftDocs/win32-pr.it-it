---
title: Proprietà Speed
description: Proprietà Speed
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaca342dde91965ab381f95671a39c4ba9fdcae040835f09867b3fabf5899a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745953"
---
# <a name="speed-property"></a>Proprietà Speed

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore Long Integer che specifica la velocità corrente dell'output vocale del carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Velocità_*

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà restituisce l'impostazione corrente della velocità di output di pronuncia per il carattere. Per i caratteri che usano l'output TTS, la proprietà restituisce l'impostazione di output TTS effettiva per il carattere. Se TTS non è abilitato o il carattere non supporta l'output TTS, l'impostazione riflette l'impostazione utente per la velocità di output.

Anche se l'applicazione non può scrivere questo valore, è possibile includere tag **Spd** (velocità) nel testo di output che velocizzano temporaneamente l'output per una determinata espressione. Tuttavia, l'uso del tag **Spd** per modificare l'output parlato del carattere non influisce **sull'impostazione della** proprietà Speed. Per altre informazioni, vedere [Tag di output vocale.](microsoft-agent-speech-output-tags.md)

 

 




