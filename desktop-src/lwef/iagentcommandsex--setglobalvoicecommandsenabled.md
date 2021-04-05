---
title: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117671"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a>IAgentCommandsEx::SetGlobalVoiceCommandsEnabled

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

Imposta la proprietà [**Enabled**](enabled-property.md) per la grammatica vocale dei comandi globali di Microsoft Agent.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*
</dt> <dd>

Valore booleano che specifica se la grammatica vocale dei comandi globali dell'agente è abilitata. **True** Abilita la grammatica vocale; **False** lo Disabilita.

</dd> </dl>

Microsoft Agent aggiunge automaticamente i parametri vocali (grammatica) per l'apertura e la chiusura della finestra dei comandi vocali e per visualizzare e nascondere il carattere. Se impostato su **false**, Agent Disabilita tutti i parametri vocali per questi comandi, nonché i parametri vocali per la [**didascalia**](caption-property.md) degli oggetti [**comando**](/windows/desktop/lwef/the-command-object) di altri client. In questo modo è possibile eliminarli dalla grammatica attiva corrente del client. Tuttavia, poiché questo potrebbe bloccare l'accesso vocale ad altri client, reimpostare questa proprietà su **true** dopo l'elaborazione dell'input vocale dell'utente.

La disabilitazione della proprietà non influisce sul menu di scelta rapida del carattere. Verranno comunque visualizzati i comandi globali aggiunti dal server. Non è possibile rimuoverli dal menu a comparsa.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 