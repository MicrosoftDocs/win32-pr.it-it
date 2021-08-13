---
title: Metodo StopAll
description: Metodo StopAll
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b138be6ea75135d5ddefdea9e1e5cc120d875ae092478ad3147332720e5a0907
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745943"
---
# <a name="stopall-method"></a>Metodo StopAll

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Arresta tutte le richieste di animazione o i tipi specificati di richieste per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Tipo StopAll_ *  \[ \]



| Parte   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Tipo* | facoltativo. Per usare questo parametro, è possibile usare uno dei valori seguenti. È anche possibile specificare più tipi separandoli con virgole. <br/> "**Get**" <br/> Per arrestare tutte le richieste [**Get in**](get-method.md) coda.<br/> "**NonQueuedGet**" <br/> Per arrestare tutte le richieste [**Get**](get-method.md) non in coda (**Metodo Get** con il **parametro Queue** impostato su **False**).<br/> "**Move**" <br/> Per arrestare tutte le richieste [**MoveTo**](moveto-method.md) in coda.<br/> "**Play**" <br/> Per arrestare tutte le richieste [**play in**](play-method.md) coda.<br/> "**Speak**" <br/> Per arrestare tutte le richieste [**Speak in**](speak-method.md) coda.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se non si imposta il parametro **Type,** il server arresta tutte le animazioni per il carattere, incluse le richieste [**Get**](get-method.md) in coda e non in coda, e cancella la coda di animazione. Interrompe anche la riproduzione dell'animazione Nascondi o Mostra di un carattere.

Questo metodo non genererà un [**oggetto Request.**](/windows/desktop/lwef/the-request-object)

## <a name="see-also"></a>Vedere anche

[**Metodo Stop**](stop-method.md)


 

