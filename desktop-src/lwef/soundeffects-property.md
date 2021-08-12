---
title: Proprietà SoundEffects
description: Proprietà SoundEffects
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3894782ec3a038831f7bab7d6d5fe0701936baf1c1add136ad5c2c3446f78867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246257"
---
# <a name="soundeffects-property"></a>Proprietà SoundEffects

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce un valore booleano che indica se gli effetti sonori (. WAV) configurati come parte delle azioni di un carattere verranno riprodotti.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. AudioOutput.SoundEffects**



| Valore     | Descrizione                          |
|-----------|--------------------------------------|
| **True**  | Gli effetti sonori dei caratteri sono abilitati. |
| **False** | L'effetto sonoro carattere è disabilitato. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa proprietà riflette l'opzione Riproduci effetti audio carattere nella pagina Output della finestra delle proprietà agente (Opzioni carattere avanzate). Quando la **proprietà SoundEffects** restituisce **True,** verranno riprodotti gli effetti audio inclusi nella definizione di un carattere. Se **false,** gli effetti sonori non verranno riprodotti. L'impostazione della proprietà influisce su tutti i caratteri ed è di sola lettura. solo l'utente può impostare il valore di questa proprietà.

## <a name="see-also"></a>Vedere anche

[**Evento AgentPropertyChange**](agentpropertychange-event.md)


 

 




