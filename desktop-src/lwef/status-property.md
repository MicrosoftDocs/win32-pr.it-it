---
title: Proprietà Status
description: Proprietà Status
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edb1196e5ec41571c9c760b91a72b350b94f6b85f1f85af018691d3f25ecec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245825"
---
# <a name="status-property"></a>Proprietà Status

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce lo stato del canale di output audio.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. AudioOutput.Status**



| Valore | Descrizione                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| 0     | Il canale di output audio è disponibile (non occupato).                                                                 |
| 1     | Non è disponibile alcun supporto per l'output audio. ad esempio perché non è presente alcuna scheda audio.                                |
| 2     | Il canale di output audio non può essere aperto (è occupato); ad esempio perché un'altra applicazione riproduce l'audio. |
| 3     | Il canale di output audio è occupato perché il server sta elaborando l'input vocale dell'utente.                              |
| 4     | Il canale di output audio è occupato perché un carattere sta parlando.                                       |
| 5     | Il canale di output audio non è occupato, ma è in attesa dell'input vocale dell'utente.                                    |
| 6     | Si è verificato un altro problema (sconosciuto) durante il tentativo di accesso al canale di output audio.                          |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa impostazione consente all'applicazione client di eseguire query sul canale di output audio, restituisce un valore Integer che indica lo stato del canale di output audio. È possibile usarlo per determinare se è appropriato che il tuo carattere dia voce o se è appropriato provare ad attivare la modalità di ascolto (usando il [**metodo Listen).**](listen-method.md)

## <a name="see-also"></a>Vedere anche

[**Evento ListenComplete**](listencomplete-event.md)


 

 




