---
title: Metodo Insert
description: Metodo Insert
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94b63da0477ee048239afa34ff57475dcce8f0d1129f4574d6b7b6543d75e49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114631"
---
# <a name="insert-method"></a>Metodo Insert

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Inserisce un **oggetto Command** nella **raccolta Commands.**

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Commands.Insert_ *  *Name*, *RefName*, *Before*\_

*Caption*, *Voice, Enabled, Visible*



| Parte      | Descrizione                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nome*    | Obbligatorio. Valore stringa corrispondente all'ID assegnato al [**comando**](/windows/desktop/lwef/the-command-object).                                                                                                                                                                                               |
| *Refname* | Obbligatorio. Valore stringa corrispondente al nome (ID) del comando appena sopra o sotto il punto in cui si vuole inserire il nuovo comando.                                                                                                                                                                 |
| *Prima*  | facoltativo. Valore booleano che indica se inserire il nuovo comando prima del comando specificato da *RefName.* **True** (impostazione predefinita). Il nuovo comando verrà inserito prima del comando a cui si fa riferimento.<br/> **False** Il nuovo comando verrà inserito dopo il comando a cui si fa riferimento.<br/> |
| *Didascalia* | facoltativo. Valore stringa corrispondente al nome che verrà visualizzato nel menu a comparsa del carattere e nella finestra comandi quando l'applicazione client è attiva per l'input. Per altre informazioni, vedere la [**proprietà Caption**](/windows/desktop/lwef/the-command-object) dell'oggetto [**Command.**](caption-property.md)    |
| *Chiamata vocale*   | facoltativo. Valore stringa corrispondente alle parole o alla frase che devono essere usate dal motore di riconoscimento vocale per il riconoscimento di questo comando. Per altre informazioni sulla formattazione delle alternative per la stringa, vedere la [**proprietà**](/windows/desktop/lwef/the-command-object) Voice dell'oggetto **Command.**                                  |
| *Enabled* | facoltativo. Valore booleano che indica se il comando è abilitato. Il valore predefinito è **True**. Per altre informazioni, vedere la [**proprietà**](/windows/desktop/lwef/the-command-object) Enabled **dell'oggetto** Command.                                                                                                  |
| *Visible* | facoltativo. Valore booleano che indica se il comando è visibile nella finestra Comandi quando l'applicazione client è attiva per l'input. Il valore predefinito è **True**. Per altre informazioni, vedere la [**proprietà**](/windows/desktop/lwef/the-command-object) Visible [**dell'oggetto**](visible-property.md) Command.       |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il valore della proprietà [**Name di**](/windows/desktop/lwef/the-command-object) un oggetto [**Command**](name-property.md) deve essere univoco all'interno della [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object) È necessario rimuovere un **comando prima** di poter creare un nuovo **comando con** la stessa impostazione **della** proprietà Name. Il tentativo di creare **un comando** con una **proprietà Name** già esistente genera un errore.

Questo metodo restituisce anche un [**oggetto**](/windows/desktop/lwef/the-command-object) Command. In questo modo è possibile dichiarare un oggetto e assegnare un **comando** quando si chiama il **metodo Insert.**


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a>Vedere anche

[**Metodo Add,**](add-method.md) [**Metodo Remove,**](remove-method.md) [**Metodo RemoveAll**](removeall-method.md)


 

