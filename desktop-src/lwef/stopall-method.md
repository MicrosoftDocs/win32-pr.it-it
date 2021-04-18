---
title: Metodo StopAll
description: Metodo StopAll
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c99a687c2481d9686e84b7fa5c198e7a4273a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299594"
---
# <a name="stopall-method"></a>Metodo StopAll

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Arresta tutte le richieste di animazione o i tipi di richieste specificati per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *").* *  \[ *Tipo* stopAll\]



| Parte   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Tipo* | facoltativo. Per utilizzare questo parametro, è possibile utilizzare uno dei valori seguenti. È anche possibile specificare più tipi separandoli con virgole. <br/> "**Get**" <br/> Per arrestare tutte le richieste [**Get**](get-method.md) in coda.<br/> "**NonQueuedGet**" <br/> Per arrestare tutte le richieste [**Get**](get-method.md) non accodate (metodo **Get** con parametro **queue** impostato su **false**).<br/> "**Sposta**" <br/> Per arrestare tutte le richieste [**movete**](moveto-method.md) in coda.<br/> "**Riproduci**" <br/> Per arrestare tutte le richieste di [**riproduzione**](play-method.md) in coda.<br/> "**Pronuncia**" <br/> Per arrestare tutte le richieste [**Speak**](speak-method.md) in coda.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se non si imposta il parametro di **tipo** , il server interrompe tutte le animazioni per il carattere, incluse le richieste [**Get**](get-method.md) in coda e non accodate, e cancella la coda di animazioni. Interrompe inoltre la riproduzione dell'animazione di un carattere o di una visualizzazione.

Questo metodo non genererà un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .

## <a name="see-also"></a>Vedere anche

[**Metodo Stop**](stop-method.md)


 

