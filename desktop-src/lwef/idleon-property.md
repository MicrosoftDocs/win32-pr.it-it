---
title: Proprietà IdleOn
description: Proprietà IdleOn
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7fcec4bd6e163baab7722e4d893146819408a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328196"
---
# <a name="idleon-property"></a>Proprietà IdleOn

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore booleano che determina se il server gestisce le animazioni di stato **minimo** del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). IdleOn*( *  \[  =  *booleano* )\]

</dd> </dl> 

| Parte      | Descrizione                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se il server gestisce la modalità di inattività. **True** (impostazione predefinita) la gestione del server dello stato inattivo è abilitata. <br/> **False** La gestione del server dello stato inattivo è disabilitata. <br/> |



 

## <a name="remarks"></a>Commenti

Il server imposta automaticamente un timeout dopo l'ultima animazione riprodotta per un carattere. Quando l'intervallo di questo timer è completo, il server inizia **lo stato di** inattivo per un carattere, eseguendo le animazioni al **minimo** associate a intervalli regolari. Se si desidera disabilitare il server **per la riproduzione** automatica delle animazioni di stato di inattivo, impostare la proprietà su **false** e riprodurre un'animazione oppure chiamare il metodo [**Stop**](stop-method.md) . L'impostazione di questo valore non influisce sullo stato di animazione corrente del carattere.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

 

 





