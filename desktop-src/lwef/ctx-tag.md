---
title: CTX (tag)
description: CTX (tag)
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16beae0fd4ccc062969d9aafb4d8747e4c5afe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044954"
---
# <a name="ctx-tag"></a>CTX (tag)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Imposta il contesto del testo di output.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

\\**Ctx** = *stringa* di\\



| Parte     | Descrizione                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Stringa che specifica il contesto del testo che segue, che determina il modo in cui vengono pronunciati simboli o abbreviazioni.<br/> **"Indirizzo"**    Indirizzi e/o numeri di telefono.<br/> **"Posta elettronica"**    Posta elettronica.<br/> Il contesto **"Unknown"** (impostazione predefinita) è sconosciuto.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo tag è supportato solo per l'output generato da TTS. L'intervallo di valori per il parametro può variare a seconda del motore TTS installato.

 

 





