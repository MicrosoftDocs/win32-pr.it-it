---
title: Oggetto Command
description: Oggetto Command
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299698"
---
# <a name="the-command-object"></a>Oggetto Command

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Un oggetto [**Command**](/windows/desktop/lwef/the-command-object) è un elemento in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . Il server consente all'utente di accedere agli oggetti **Command** quando l'applicazione client diventa attiva.

-   [Proprietà oggetto comando](command-object-properties.md)

Per accedere alla proprietà di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) , è possibile farvi riferimento nella relativa raccolta usando la relativa proprietà [**Name**](name-property.md) . In VBScript e Visual Basic è possibile usare direttamente la proprietà **Name** :


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Per i linguaggi di programmazione che non supportano le raccolte, usare il metodo di [**comando**](command-method.md) :


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



È anche possibile fare riferimento a un oggetto comando creando un riferimento a esso. In Visual Basic dichiarare una variabile oggetto e utilizzare l'istruzione set per creare il riferimento:


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



In Visual Basic 5,0, è anche possibile dichiarare l'oggetto come tipo [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) e creare il riferimento. Questa convenzione Abilita il binding anticipato, con conseguente miglioramento delle prestazioni:


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



In VBScript è possibile dichiarare un riferimento come un particolare tipo, ma è comunque possibile dichiarare la variabile e impostarla sul [**comando**](/windows/desktop/lwef/the-command-object) nella raccolta:


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



Un comando può essere visualizzato nel menu di scelta rapida del carattere e nella finestra comandi oppure in entrambi. Per visualizzare nel menu a comparsa, deve avere una didascalia e impostare la proprietà [**Visible**](visible-property.md) su **true**. Inoltre, la proprietà **Visible** dell'oggetto raccolta Commands deve essere impostata su **true**. Per visualizzare nella finestra dei comandi, è necessario impostare le proprietà [**Caption**](caption-property.md) e [**Voice**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object) . Si noti che le voci di menu popup di un carattere non cambiano mentre il menu viene visualizzato. Se si aggiungono o si rimuovono i comandi o se ne modificano le proprietà quando viene visualizzato il menu popup del carattere, il menu Visualizza tali modifiche ogni volta che l'utente lo Visualizza. Tuttavia, la finestra comandi riflette in modo dinamico tutte le modifiche apportate.

Nella tabella seguente viene riepilogato il modo in cui le proprietà di un [**comando**](/windows/desktop/lwef/the-command-object) influiscono sulla presentazione:



Proprietà Caption

Proprietà Voice-Caption

Proprietà Voice

Visible (proprietà)

Proprietà Enabled

Viene visualizzato nel menu a comparsa del carattere

Viene visualizzato nella finestra comandi

Sì

Sì

Sì

True

True

Normale, uso della [ **didascalia**](caption-property.md)

Sì, uso di [ **VoiceCaption**](voicecaption-property.md)

Sì

Sì

Sì

Vero

Falso

Disabilitato, utilizzo della [ **didascalia**](caption-property.md)

No

Sì

Sì

Sì

False

True

Non viene visualizzato

Sì, uso di [ **VoiceCaption**](voicecaption-property.md)

Sì

Sì

Sì

False

False

Non viene visualizzato

No

Sì

Sì

No 

True

True

Normale, uso della [ **didascalia**](caption-property.md)

No

Sì

Sì

No 

Vero

Falso

Disabilitato, utilizzo della [ **didascalia**](caption-property.md)

No

Sì

Sì

No 

False

True

Non viene visualizzato

No

Sì

Sì

No 

False

False

Non viene visualizzato

No

No 

Sì

Sì

True

True

Non viene visualizzato

Sì, uso di [ **VoiceCaption**](voicecaption-property.md)

No 

Sì

Sì

Vero

Falso

Non viene visualizzato

No

No 

Sì

Sì

False

True

Non viene visualizzato

Sì, uso di [ **VoiceCaption**](voicecaption-property.md)

No 

Sì

Sì

False

False

Non viene visualizzato

No

No 

Sì

No 

True

True

Non viene visualizzato

No

No 

Sì

No 

Vero

Falso

Non viene visualizzato

No

No 

Sì

No 

False

True

Non viene visualizzato

No

No 

Sì

No 

False

False

Non viene visualizzato

No

Sì

No 

Sì

True

True

Normale, uso della [ **didascalia**](caption-property.md)

Sì, uso della [ **didascalia**](caption-property.md)

Sì

No 

Sì

Vero

Falso

Disabilitato, utilizzo della [ **didascalia**](caption-property.md)

No

Sì

No 

Sì

False

True

Non viene visualizzato

Sì, uso della [ **didascalia**](caption-property.md)

Sì

No 

Sì

False

False

Non viene visualizzato

No

Sì

No 

No 

True

True

Normale, uso della [ **didascalia**](caption-property.md)

No

Sì

No 

No 

Vero

Falso

Disabilitato, utilizzo della [ **didascalia**](caption-property.md)

No

Sì

No 

No 

False

True

Non viene visualizzato

No

Sì

No 

No 

False

False

Non viene visualizzato

No

No 

No 

Sì

True

True

Non viene visualizzato

No 

No 

No 

Sì

Vero

Falso

Non viene visualizzato

No

No 

No 

Sì

False

True

Non viene visualizzato

No 

No 

No 

Sì

False

False

Non viene visualizzato

No

No 

No 

No 

True

True

Non viene visualizzato

No

No 

No 

No 

Vero

Falso

Non viene visualizzato

No

No 

No 

No 

False

True

Non viene visualizzato

No

No 

No 

No 

False

False

Non viene visualizzato

No

 Se l'impostazione della proprietà è null. In alcuni linguaggi di programmazione è possibile che una stringa vuota non venga interpretata come una stringa null.  Il comando è ancora accessibile tramite voce.<br/>



 

Quando il server riceve l'input per uno dei comandi, invia un evento di [**comando**](/windows/desktop/lwef/the-command-object) e passa di nuovo il nome del **comando** come attributo dell'oggetto [**userinput**](/windows/desktop/lwef/iagentuserinput) . È quindi possibile usare le istruzioni condizionali per trovare una corrispondenza ed elaborare il **comando**.

 

