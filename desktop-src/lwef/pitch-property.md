---
title: Proprietà Pitch
description: Proprietà Pitch
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e346ea0fbb7ebb819d8f00b2fc6aab1ab95e72f391bddc696da18a49f0b2a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475411"
---
# <a name="pitch-property"></a>Proprietà Pitch

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Descrizione** 
</dt> <dd>

Restituisce un valore Long Integer per l'impostazione del passo dell'output vocale (TTS) del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Tono_*

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà si applica solo ai caratteri configurati per l'output TTS. Se il carattere non supporta l'output TTS, questa proprietà restituisce zero (0).

Anche se l'applicazione non può scrivere questo valore, è possibile includere tag **Pit** (pitch) nel testo di output che aumenterà temporaneamente l'tono per una determinata espressione. Tuttavia, l'uso del tag **Pit** per modificare il passo non modificherà l'impostazione **della** proprietà Pitch. Per altre informazioni, vedere [Tag di output vocale.](pit-tag.md)

 

 




