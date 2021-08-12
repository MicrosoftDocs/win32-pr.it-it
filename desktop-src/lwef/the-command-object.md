---
title: Oggetto Command
description: Oggetto Command
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242a90022431b826cf877edd862cd89a39d193865ed31afc1e4ff911f4189756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245617"
---
# <a name="the-command-object"></a>Oggetto Command

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Un [**oggetto Command**](/windows/desktop/lwef/the-command-object) è un elemento di una raccolta [**Commands.**](/windows/desktop/lwef/the-commands-collection-object) Il server fornisce all'utente l'accesso agli **oggetti Command** quando l'applicazione client diventa attiva per l'input.

-   [Proprietà dell'oggetto Command](command-object-properties.md)

Per accedere alla proprietà di un [**oggetto Command,**](/windows/desktop/lwef/the-command-object) è necessario fare riferimento a esso nella relativa raccolta usando la [**relativa proprietà**](name-property.md) Name. In VBScript e Visual Basic è possibile usare direttamente la **proprietà** Name:


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Per i linguaggi di programmazione che non supportano le raccolte, usare il [**metodo Command:**](command-method.md)


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



È anche possibile fare riferimento a un oggetto Command creando un riferimento a esso. In Visual Basic dichiarare una variabile oggetto e usare l'istruzione Set per creare il riferimento:


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



In Visual Basic 5.0 è anche possibile dichiarare l'oggetto come tipo [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) e creare il riferimento. Questa convenzione abilita l'associazione anticipata, che comporta prestazioni migliori:


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



In VBScript è possibile dichiarare un riferimento come tipo specifico, ma è comunque possibile dichiarare la variabile e impostarla sul [**comando**](/windows/desktop/lwef/the-command-object) nella raccolta:


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



Un comando può essere visualizzato nel menu a comparsa del carattere e nella finestra comandi o in entrambi. Per essere visualizzato nel menu a comparsa, deve avere una didascalia e la [**proprietà Visible**](visible-property.md) deve essere impostata su **True.** Inoltre, anche la relativa proprietà **Visible dell'oggetto raccolta Commands** deve essere impostata su **True.** Per essere visualizzato nella finestra Comandi, è necessario [**che le proprietà Didascalia**](/windows/desktop/lwef/the-command-object) e [**Voce**](voice-property.md) di un comando vengano impostate. [](caption-property.md) Si noti che le voci del menu a comparsa di un carattere non cambiano mentre viene visualizzato il menu. Se si aggiungono o rimuovono comandi o si modificano le proprietà mentre viene visualizzato il menu a comparsa del carattere, il menu visualizza le modifiche ogni volta che l'utente lo visualizza. Tuttavia, la finestra Comandi riflette dinamicamente tutte le modifiche apportate.

La tabella seguente riepiloga il modo in cui le proprietà di un [**comando influiscono**](/windows/desktop/lwef/the-command-object) sulla relativa presentazione:



Proprietà Caption

Voice-Caption proprietà

Proprietà Voice

Proprietà Visible

Proprietà Enabled

Viene visualizzato nel menu a comparsa del carattere

Viene visualizzato nella finestra Comandi

Sì

Sì

Sì

True

True

Normal, uso di [ **Caption**](caption-property.md)

Sì, con [ **VoiceCaption**](voicecaption-property.md)

Sì

Sì

Sì

Vero

Falso

Disabilitato, con [ **Didascalia**](caption-property.md)

No

Sì

Sì

Sì

False

True

Non viene visualizzato

Sì, con [ **VoiceCaption**](voicecaption-property.md)

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

Normal, uso di [ **Caption**](caption-property.md)

No

Sì

Sì

No 

Vero

Falso

Disabilitato, con [ **Didascalia**](caption-property.md)

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

Sì, con [ **VoiceCaption**](voicecaption-property.md)

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

Sì, con [ **VoiceCaption**](voicecaption-property.md)

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

Normale, con [ **Didascalia**](caption-property.md)

Sì, usando [ **Didascalia**](caption-property.md)

Sì

No 

Sì

Vero

Falso

Disabilitato, con [ **Didascalia**](caption-property.md)

No

Sì

No 

Sì

False

True

Non viene visualizzato

Sì, usando [ **Didascalia**](caption-property.md)

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

Normale, con [ **Didascalia**](caption-property.md)

No

Sì

No 

No 

Vero

Falso

Disabilitato, con [ **Didascalia**](caption-property.md)

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

 Se l'impostazione della proprietà è Null. In alcuni linguaggi di programmazione una stringa vuota potrebbe non essere interpretata come una stringa Null.  Il comando è ancora accessibile tramite voce.<br/>



 

Quando il server riceve l'input per uno dei comandi, invia un evento [**Command**](/windows/desktop/lwef/the-command-object) e restituisce il nome dell'oggetto **Command** come attributo [**dell'oggetto UserInput.**](/windows/desktop/lwef/iagentuserinput) È quindi possibile usare istruzioni condizionali per trovare la corrispondenza con il comando ed **elaborarvi.**

 

