---
title: Insert (metodo)
description: Insert (metodo)
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74eb6d76c1be9b83b7742255ee5a771ed93c64d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299768"
---
# <a name="insert-method"></a>Insert (metodo)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Inserisce un oggetto **Command** nell'insieme **Commands** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). Commands. Insert* *  *Name*, *refname*, *before*\_

*Didascalia*, *voce, abilitata, visibile*



| Parte      | Descrizione                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nome*    | Obbligatorio. Valore stringa corrispondente all'ID assegnato al [**comando**](/windows/desktop/lwef/the-command-object).                                                                                                                                                                                               |
| *RefName* | Obbligatorio. Valore stringa corrispondente al nome (ID) del comando appena sopra o al di sotto del quale si desidera inserire il nuovo comando.                                                                                                                                                                 |
| *Prima*  | facoltativo. Valore booleano che indica se inserire il nuovo comando prima del comando specificato da *refname*. **True** (impostazione predefinita). Il nuovo comando verrà inserito prima del comando a cui si fa riferimento.<br/> **False** Il nuovo comando verrà inserito dopo il comando a cui si fa riferimento.<br/> |
| *Didascalia* | facoltativo. Valore stringa corrispondente al nome che verrà visualizzato nel menu di scelta rapida del carattere e nella finestra comandi quando l'applicazione client è di input-attivo. Per ulteriori informazioni, vedere la proprietà [**Caption**](caption-property.md)dell'oggetto [**comando**](/windows/desktop/lwef/the-command-object) .    |
| *Chiamata vocale*   | facoltativo. Valore stringa corrispondente alle parole o alla frase che deve essere utilizzata dal motore di riconoscimento vocale per il riconoscimento di questo comando. Per ulteriori informazioni sulla formattazione di alternative per la stringa, vedere la proprietà **Voice** dell'oggetto [**comando**](/windows/desktop/lwef/the-command-object) .                                  |
| *Enabled* | facoltativo. Valore booleano che indica se il comando è abilitato. Il valore predefinito è **True**. Per ulteriori informazioni, vedere la proprietà **Enabled** dell'oggetto [**Command**](/windows/desktop/lwef/the-command-object) .                                                                                                  |
| *Visible* | facoltativo. Valore booleano che indica se il comando è visibile nella finestra dei comandi quando l'applicazione client è di input-attivo. Il valore predefinito è **True**. Per ulteriori informazioni, vedere la proprietà [**Visible**](visible-property.md) dell'oggetto [**comando**](/windows/desktop/lwef/the-command-object) .       |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il valore della proprietà [**Name**](name-property.md) di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) deve essere univoco all'interno della relativa raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . Prima di poter creare un nuovo **comando** con la stessa impostazione della proprietà **Name** , è necessario rimuovere un **comando** . Il tentativo di creare un **comando** con una proprietà **Name** già esistente genera un errore.

Questo metodo restituisce anche un oggetto [**Command**](/windows/desktop/lwef/the-command-object) . In questo modo è possibile dichiarare un oggetto e assegnarvi un **comando** quando si chiama il metodo **Insert** .


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a>Vedere anche

Metodo [**Add**](add-method.md), [**Remove**](remove-method.md), metodo [**RemoveAll**](removeall-method.md)


 

