---
title: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7275bfe28190e06782cb2564dbf4868dd2c096
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398946"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a>IAgentCommandsEx::GetGlobalVoiceCommandsEnabled

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

Recupera un valore che indica se la grammatica vocale per i comandi globali dell'agente è abilitata.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Indirizzo che riceve **true** se la grammatica vocale per i comandi globali dell'agente è abilitata, **false** se è disabilitata.

</dd> </dl>

Microsoft Agent aggiunge automaticamente i parametri vocali (grammatica) per l'apertura e la chiusura della finestra dei comandi vocali e per visualizzare e nascondere il carattere. Quando questo metodo restituisce **false**, tutti i parametri vocali per questi comandi e i parametri vocali per la [**didascalia**](caption-property.md) degli oggetti [**comando**](/windows/desktop/lwef/the-command-object) di altri client non sono inclusi nella grammatica. In questo modo è possibile eliminarli dalla grammatica attiva corrente del client. Questa impostazione non riflette tuttavia l'inclusione di questi comandi nel menu di scelta rapida del carattere.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 