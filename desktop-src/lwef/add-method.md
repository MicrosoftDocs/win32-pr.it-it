---
title: Aggiungi metodo
description: Aggiungi metodo
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ae6cc3cd0a39be8b293a6ae64a96859e5d4fcf6d23ff410439422676b3527e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976831"
---
# <a name="add-method"></a>Aggiungi metodo

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Aggiunge un [oggetto Command](the-command-object.md) alla [raccolta Commands.](the-commands-collection-object.md)

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Commands.Add_ *  *Name,* *Caption,* *Voice,* *Enabled,* *Visible*



| Parte      | Descrizione                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nome*    | Obbligatorio. Valore stringa corrispondente all'ID assegnato per il comando.                                                                                                                                                                                                                                        |
| *Didascalia* | facoltativo. Valore stringa corrispondente al nome che verrà visualizzato nel menu a comparsa del carattere e nella finestra comandi quando l'applicazione client è attiva per l'input. Per altre informazioni, vedere la [proprietà Caption](the-command-object.md) dell'oggetto [Command.](caption-property.md)                       |
| *Chiamata vocale*   | facoltativo. Valore stringa corrispondente alle parole o alla frase che devono essere usate dal motore di riconoscimento vocale per il riconoscimento di questo comando. Per altre informazioni sulla formattazione delle alternative per la stringa, vedere la [proprietà](the-command-object.md) Voice dell'oggetto [Command.](voice-property.md)                                |
| *Enabled* | facoltativo. Valore booleano che indica se il comando è abilitato. Il valore predefinito è **True**. Per altre informazioni, vedere la [proprietà](the-command-object.md) Enabled [dell'oggetto](enabled-property.md) Command.                                                                                              |
| *Visible* | facoltativo. Valore booleano che indica se il comando è visibile nel menu a comparsa del carattere quando l'applicazione client è attiva per l'input. Il valore predefinito è **True**. Per altre informazioni, vedere la [proprietà](the-command-object.md) Visible [dell'oggetto](visible-property.md) Command. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il valore della proprietà [Name di](the-command-object.md) un oggetto [Command](name-property.md) deve essere univoco all'interno della [raccolta Commands.](the-commands-collection-object.md) È necessario rimuovere un comando prima di poter creare un nuovo comando con la stessa impostazione della proprietà Name. Il tentativo di creare un comando con una proprietà Name già esistente genera un errore.

Questo metodo restituisce anche un [oggetto](the-command-object.md) Command. In questo modo è possibile dichiarare un oggetto e assegnare un comando quando si chiama il metodo Add.


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

[**Metodo Remove**](remove-method.md)
</dt> </dl>

 

 




