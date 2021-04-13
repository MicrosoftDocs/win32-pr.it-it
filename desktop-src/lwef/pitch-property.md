---
title: Pitch (proprietà)
description: Pitch (proprietà)
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 998ee4bcf77878062425086d67066040f5d58421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396890"
---
# <a name="pitch-property"></a>Pitch (proprietà)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Descrizione** 
</dt> <dd>

Restituisce un valore long integer per l'impostazione del pitch di output vocale del carattere specificato (TTS).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). Passo**

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà si applica solo ai caratteri configurati per l'output TTS. Se il carattere non supporta l'output TTS, questa proprietà restituisce zero (0).

Anche se l'applicazione non è in grado di scrivere questo valore, è possibile includere tag **Pit** (pitch) nel testo di output che aumenterà temporaneamente il pitch per una determinata espressione. Tuttavia, se si usa il tag **Pit** per modificare il pitch, l'impostazione della proprietà **pitch** non cambierà. Per altre informazioni, vedere [tag di output vocale](pit-tag.md).

 

 




