---
title: Listen (metodo)
description: Listen (metodo)
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813fb155074c4cc47a51ec7241eddd332edbcc3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046615"
---
# <a name="listen-method"></a>Listen (metodo)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Attiva la modalità di ascolto (riconoscimento vocale) per un periodo di tempo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente. ***Caratteri * * * * ("*** CharacterID * * *").* *  *Stato* ascolto



| Parte    | Descrizione                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *State* | Obbligatorio. Valore booleano che determina se attivare o disattivare la modalità di ascolto. Valore **true** Attiva la modalità di ascolto. <br/> **False** Disattiva la modalità di ascolto.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

L'impostazione di questo metodo su **true** Abilita la modalità di ascolto (attiva il riconoscimento vocale) per un periodo di tempo fisso (10 secondi). Anche se non è possibile impostare il valore del timeout, è possibile disattivare la modalità di ascolto prima della scadenza del timeout. Se un utente (o un altro client) ha impostato correttamente la modalità di ascolto e si tenta di impostare questa proprietà su **true** prima della scadenza del timeout, il metodo ha esito positivo e reimposta il timeout. Tuttavia, se la modalità di ascolto è attiva perché l'utente preme il tasto ascolto, il metodo ha esito positivo, ma il timeout viene ignorato e la modalità di ascolto termina in base all'interazione dell'utente con la chiave di ascolto.

Questo metodo ha esito positivo solo quando viene chiamato dal client di input-attivo e se i servizi di riconoscimento vocale sono stati avviati. Per assicurarsi che i servizi di riconoscimento vocale siano stati avviati, eseguire una query o impostare il [**SRModeID**](srmodeid-property.md) o impostare l'impostazione [**Voice**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object) prima di chiamare **Listen** altrimenti il metodo avrà esito negativo. Per rilevare l'esito positivo di questo metodo, chiamarlo come funzione e restituirà un valore booleano che indica se il metodo ha avuto esito positivo.


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



Il metodo ha esito negativo anche se l'utente preme il tasto di attesa e si tenta di impostare **Listen** su **false**. Tuttavia, se l'utente ha rilasciato il tasto ascolto e la modalità di ascolto non è scaduta, l'operazione avrà esito positivo.

**Listen** ha esito negativo anche se non è disponibile un motore vocale compatibile che corrisponda all'impostazione [**LanguageID**](languageid-property.md) del carattere, l'utente ha disabilitato l'input vocale usando la finestra delle proprietà di Microsoft Agent oppure il dispositivo audio è occupato.

Quando si imposta correttamente questo metodo su **true**, il server attiva l'evento [**ListenStart**](listenstart-event.md) . Il server invia [**ListenComplete**](listencomplete-event.md) quando il timeout della modalità di ascolto viene completato o quando si imposta **Listen** su **false**.

Questo metodo non chiama automaticamente [**Interrompi**](stop-method.md) e riproduce un'animazione dello stato di ascolto come il server quando viene premuto il tasto di attesa. Questo consente di determinare se interrompere l'animazione corrente usando l'animazione [**ListenStart**](listenstart-event.md) chiamando **Interrompi** e riproducendo un'animazione appropriata. Tuttavia, il server chiama **Stop** e riproduce un'animazione dello stato di udito quando viene rilevata un'espressione utente.

## <a name="see-also"></a>Vedere anche

[**Proprietà LanguageID**](languageid-property.md), [**evento ListenComplete**](listencomplete-event.md), [**evento ListenStart**](listenstart-event.md)


 

