---
title: Proprietà Status
description: Proprietà Status
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402e88185e1024aa5958d06936a6529ae4012622
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298461"
---
# <a name="status-property"></a>Proprietà Status

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce lo stato del canale di output audio.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente * * *. AudioOutput. status**



| Valore | Descrizione                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| 0     | Il canale di output audio è disponibile (non occupato).                                                                 |
| 1     | Non è disponibile alcun supporto per l'output audio. ad esempio, perché non è presente alcuna scheda audio.                                |
| 2     | Non è possibile aprire il canale di output audio (è occupato); ad esempio, perché un'altra applicazione sta riproducendo audio. |
| 3     | Il canale di output audio è occupato perché il server sta elaborando l'input vocale dell'utente.                              |
| 4     | Il canale di output audio è occupato perché è in corso un carattere.                                       |
| 5     | Il canale di output audio non è occupato, ma è in attesa dell'input vocale dell'utente.                                    |
| 6     | Si è verificato un altro problema (sconosciuto) durante il tentativo di accedere al canale di output audio.                          |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa impostazione consente all'applicazione client di eseguire una query sul canale di output audio, restituendo un valore integer che indica lo stato del canale di output audio. È possibile usare questo valore per determinare se è opportuno che il carattere parli o se è appropriato provare ad attivare la modalità di ascolto (usando il metodo [**Listen**](listen-method.md) ).

## <a name="see-also"></a>Vedere anche

[**Evento ListenComplete**](listencomplete-event.md)


 

 




