---
title: Metodo Listen
description: Metodo Listen
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc87a57d1ebdd3f36a2d56d85e0754f5005fd6c356fc9af98760bd0db90605f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748661"
---
# <a name="listen-method"></a>Metodo Listen

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Attiva la modalità di ascolto (riconoscimento vocale) per un periodo di tempo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent.***Characters****("**_CharacterID_*_"). Stato_ *  *di ascolto*



| Parte    | Descrizione                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *State* | Obbligatorio. Valore booleano che determina se attivare o disattivare la modalità di ascolto. **True** Attiva la modalità di ascolto. <br/> **False** Disattiva la modalità di ascolto.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

L'impostazione di questo **metodo su True** abilita la modalità di ascolto (attiva il riconoscimento vocale) per un periodo di tempo fisso (10 secondi). Anche se non è possibile impostare il valore del timeout, è possibile disattivare la modalità di ascolto prima della scadenza del timeout. Se si imposta correttamente la modalità di ascolto su o un altro client e si tenta di impostare questa proprietà su **True** prima della scadenza del timeout, il metodo ha esito positivo e reimposta il timeout. Tuttavia, se la modalità di ascolto è attivata perché l'utente preme il tasto ascolto, il metodo ha esito positivo, ma il timeout viene ignorato e la modalità di ascolto termina in base all'interazione dell'utente con il tasto ascolto.

Questo metodo ha esito positivo solo quando viene chiamato dal client attivo per l'input e se i servizi voce sono stati avviati. Per assicurarsi che i servizi voce siano stati avviati, eseguire una [](/windows/desktop/lwef/the-command-object) query o impostare [**SRModeID**](srmodeid-property.md) o impostare l'impostazione [**Voce**](voice-property.md) per un comando prima di chiamare **Listen.** In caso contrario, il metodo avrà esito negativo. Per rilevare l'esito positivo di questo metodo, chiamarlo come funzione e restituirà un valore booleano che indica se il metodo ha avuto esito positivo.


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



Il metodo ha esito negativo anche se l'utente preme il tasto Ascolto e si tenta di impostare **Listen** su **False.** Tuttavia, se l'utente ha rilasciato la chiave di ascolto e la modalità di ascolto non è scaduta, avrà esito positivo.

**L'ascolto** non riesce anche se non è disponibile alcun motore di riconoscimento vocale compatibile che corrisponde all'impostazione [**LanguageID**](languageid-property.md) del carattere, se l'utente ha disabilitato l'input vocale usando la finestra delle proprietà di Microsoft Agent o il dispositivo audio è occupato.

Quando si imposta correttamente questo metodo su **True,** il server attiva [**l'evento ListenStart.**](listenstart-event.md) Il server invia [**ListenComplete**](listencomplete-event.md) al completamento del timeout della modalità di ascolto o quando si imposta **Listen** su **False.**

Questo metodo non chiama automaticamente [**Stop**](stop-method.md) e riproduce un'animazione dello stato di ascolto come fa il server quando viene premuto il tasto Ascolto. Ciò consente di determinare se interrompere l'animazione corrente usando l'animazione [**ListenStart**](listenstart-event.md) chiamando **Stop** e riproducendo l'animazione appropriata. Tuttavia, il server chiama **Stop** e riproduce un'animazione di stato Hearing quando viene rilevata un'espressione utente.

## <a name="see-also"></a>Vedere anche

[**Proprietà LanguageID,**](languageid-property.md) [**evento ListenComplete,**](listencomplete-event.md) [**evento ListenStart**](listenstart-event.md)


 

