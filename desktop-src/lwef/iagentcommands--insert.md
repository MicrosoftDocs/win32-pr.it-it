---
title: IAgentCommands inserimento
description: IAgentCommands inserimento
ms.assetid: f450aae4-db6f-4326-ae14-ddb68ab0953a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f15df0c24e16a7554881cf3d0e6c41c4ee42b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398928"
---
# <a name="iagentcommandsinsert"></a>IAgentCommands:: Insert

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Insert(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long dwRefID,     // reference Command for insertion
   long dBefore,     // insertion position flag
   long * pdwID      // address for variable for Command ID
);
```

Inserisce un oggetto [**Command**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR che specifica il valore del testo della [**didascalia**](caption-property.md) visualizzato per il [**comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR che specifica il valore dell'impostazione del testo [**vocale**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Espressione booleana che specifica l'impostazione [**Enabled**](enabled-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object). Se il parametro è **true**, il **comando** è abilitato e può essere selezionato. Se **false**, il **comando** è disabilitato.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Espressione booleana che specifica l'impostazione [**visibile**](visible-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object). Se il parametro è **true**, il **comando** sarà visibile nel menu popup del carattere (se viene impostata anche la proprietà [**Caption**](caption-property.md) ).

</dd> <dt>

<span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*
</dt> <dd>

ID di un [**comando**](/windows/desktop/lwef/the-command-object) utilizzato come riferimento per l'inserimento relativo del nuovo **comando**.

</dd> <dt>

<span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*
</dt> <dd>

Espressione booleana che specifica dove inserire il [**comando**](/windows/desktop/lwef/the-command-object). Se questo parametro è **true**, il nuovo **comando** viene inserito prima del **comando** a cui si fa riferimento. Se **false**, il nuovo **comando** viene inserito dopo il **comando** a cui si fa riferimento.

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Indirizzo di una variabile che riceve l'ID per il [**comando**](/windows/desktop/lwef/the-command-object)inserito.

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)


 

 