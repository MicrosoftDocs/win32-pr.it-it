---
title: Evento DeactivateInput
description: Evento DeactivateInput
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955592"
---
# <a name="deactivateinput-event"></a>Evento DeactivateInput

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando un client diventa non attivo in input.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

Agente **secondario** ** * * \_ DeactivateInput* *  **(ByVal** *CharacterID * * *)**



| Parte          | Descrizione                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere che rende il client non attivo. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Un client non input-attivo non riceve più gli eventi del mouse o della voce dal server, a meno che non diventi di nuovo input-Active. Il server invia questo evento solo al client che diventa non attivo.

Questo evento si verifica quando l'applicazione client è di input-attivo e l'utente sceglie la didascalia di un altro client nel menu di scelta rapida di un carattere o nella finestra comandi vocali oppure si chiama il metodo [**Activate**](activate-method.md) e si imposta il parametro **state** su 0. Può inoltre verificarsi quando l'utente seleziona il nome di un altro carattere facendo clic o parlando. Questo evento viene visualizzato anche quando il carattere è nascosto o un altro carattere diventa visibile.

### <a name="see-also"></a>Vedere anche

[**Evento ActivateInput**](activateinput-event.md)


 

 




