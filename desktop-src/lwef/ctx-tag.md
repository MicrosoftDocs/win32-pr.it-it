---
title: Ctx Tag
description: Ctx Tag
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7071994e741cb7dfd1147f163f0d7ef6299ec0dcb9d568ad068251d5a9436809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726101"
---
# <a name="ctx-tag"></a>Ctx Tag

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Imposta il contesto del testo di output.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

\\**Ctx** = *string*\\



| Parte     | Descrizione                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Stringa che specifica il contesto del testo seguente, che determina la modalità di pronuncia dei simboli o delle abbreviazioni.<br/> **"Address"**    Indirizzi e/o numeri di telefono.<br/> **"Posta elettronica"**    Posta elettronica.<br/> **Il contesto "Sconosciuto"**    (predefinito) è sconosciuto.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo tag è supportato solo per l'output generato da TTS. L'intervallo di valori per il parametro può variare a seconda del motore TTS installato.

 

 





