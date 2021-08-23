---
title: Evento DeactivateInput
description: Evento DeactivateInput
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94d7d4e737d83dfb734bcc5b35c60bddf96dcf8b07c43df3b89817da21b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610531"
---
# <a name="deactivateinput-event"></a>Evento DeactivateInput

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando un client diventa non attivo per l'input.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Sub** *agent*** \_ DeactivateInput* *  **(ByVal** *CharacterID***)**



| Parte          | Descrizione                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere che rende il client non attivo per l'input. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Un client non attivo per l'input non riceve più eventi relativi al mouse o al riconoscimento vocale dal server ,a meno che non diventi nuovamente attivo per l'input. Il server invia questo evento solo al client che diventa non attivo per l'input.

Questo evento si verifica quando l'applicazione client è attiva per l'input e l'utente sceglie la didascalia di un altro client nel menu a comparsa di un carattere o nella finestra comandi vocali oppure si chiama il metodo [**Activate**](activate-method.md) e si imposta il parametro **State** su 0. Può verificarsi anche quando l'utente seleziona il nome di un altro carattere facendo clic o pronunciando. Si ottiene anche questo evento quando il carattere è nascosto o un altro carattere diventa visibile.

### <a name="see-also"></a>Vedere anche

[**Evento ActivateInput**](activateinput-event.md)


 

 




