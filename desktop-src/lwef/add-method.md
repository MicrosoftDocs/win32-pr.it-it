---
title: Aggiungi metodo
description: Aggiungi metodo
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4527dec6014c93bb02b4f080e032266ea40159e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044602"
---
# <a name="add-method"></a>Aggiungi metodo

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Aggiunge un oggetto [Command](the-command-object.md) alla raccolta di [comandi](the-commands-collection-object.md) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). Comandi. aggiungere* il *  *nome*, la *didascalia*, la *voce*, *abilitata*, *visibile*



| Parte      | Descrizione                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nome*    | Obbligatorio. Valore stringa corrispondente all'ID assegnato per il comando.                                                                                                                                                                                                                                        |
| *Didascalia* | facoltativo. Valore stringa corrispondente al nome che verrà visualizzato nel menu di scelta rapida del carattere e nella finestra comandi quando l'applicazione client è di input-attivo. Per ulteriori informazioni, vedere la proprietà [Caption](caption-property.md) dell'oggetto [comando](the-command-object.md) .                       |
| *Chiamata vocale*   | facoltativo. Valore stringa corrispondente alle parole o alla frase che deve essere utilizzata dal motore di riconoscimento vocale per il riconoscimento di questo comando. Per ulteriori informazioni sulla formattazione di alternative per la stringa, vedere la proprietà [Voice](voice-property.md) dell'oggetto [comando](the-command-object.md) .                                |
| *Enabled* | facoltativo. Valore booleano che indica se il comando è abilitato. Il valore predefinito è **True**. Per ulteriori informazioni, vedere la proprietà [Enabled](enabled-property.md) dell'oggetto [Command](the-command-object.md) .                                                                                              |
| *Visible* | facoltativo. Valore booleano che indica se il comando è visibile nel menu popup del carattere per il carattere quando l'applicazione client è di tipo input-attivo. Il valore predefinito è **True**. Per ulteriori informazioni, vedere la proprietà [Visible](visible-property.md) dell'oggetto [comando](the-command-object.md) . |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il valore della proprietà [Name](name-property.md) di un oggetto [Command](the-command-object.md) deve essere univoco all'interno della relativa raccolta di [comandi](the-commands-collection-object.md) . Prima di poter creare un nuovo comando con la stessa impostazione della proprietà Name, è necessario rimuovere un comando. Il tentativo di creare un comando con una proprietà Name già esistente genera un errore.

Questo metodo restituisce anche un oggetto [Command](the-command-object.md) . In questo modo è possibile dichiarare un oggetto e assegnarvi un comando quando si chiama addMethod.


```
   Dim Cmd1 as IAgentCtlCommandEx
   Set Cmd1 = Genie.Commands.Add ("my first command", "Test", "Test", True, True)
   Cmd1.VoiceCaption = "this is a test"
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Insert (metodo)**](insert-method.md)
</dt> <dt>

[**RemoveAll, metodo**](removeall-method.md)
</dt> <dt>

[**Remove (metodo)**](remove-method.md)
</dt> </dl>

 

 




