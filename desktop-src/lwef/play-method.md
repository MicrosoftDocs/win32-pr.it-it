---
title: Metodo Play (funzionalità dell Windows legacy)
description: Metodo Play
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980c13cbf11e86a25485558fb3ff2ade703010eb180e86291f206ea152f3c0be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247087"
---
# <a name="play-method-legacy-windows-environment-features"></a>Metodo Play (funzionalità dell Windows legacy)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Riproduce l'animazione specificata per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Play_* "*AnimationName*"

</dd> </dl> 

| Parte            | Descrizione                                                          |
|-----------------|----------------------------------------------------------------------|
| *AnimationName* | Obbligatorio. Stringa che specifica il nome di una sequenza di animazione. |



 

## <a name="remarks"></a>Commenti

Il nome di un'animazione viene definito quando il carattere viene compilato con l'editor di caratteri di Microsoft Agent. Prima di riprodurre l'animazione specificata, il server tenta di riprodurre l'animazione **Return** per l'animazione precedente, se ne è stata assegnata una.

Quando si accede alle animazioni di un carattere usando un protocollo di file convenzionale, è sufficiente usare il metodo **Play** specificando il nome dell'animazione. Tuttavia, se si usa il protocollo HTTP per accedere ai dati di animazione dei caratteri, usare il **metodo Get** per caricare l'animazione prima di chiamare il **metodo Play.**

Per altre informazioni, vedere il **metodo Get.**

Per semplificare la sintassi, è possibile dichiarare un riferimento a un oggetto e impostarlo in modo che punti all'oggetto [**Character**](/windows/desktop/lwef/the-characters-object) nella raccolta [**Characters**](/windows/desktop/lwef/the-characters-object) e usare il riferimento come parte delle **istruzioni Play:**


```
   Dim Genie   
   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")
   
   Genie.Get "state", "Showing"
   Genie.Show

   Genie.Get "animation", "Greet, GreetReturn"
   Genie.Play "Greet"
   Genie.Speak "Hello."
```



Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un [**oggetto Request.**](/windows/desktop/lwef/the-request-object) Inoltre, se si specifica un'animazione non caricata o se il carattere non è  stato caricato correttamente, il server imposta la proprietà [**Status**](status-property.md) dell'oggetto Request su "failed" con un numero di errore appropriato. Tuttavia, se l'animazione non esiste e i dati del carattere sono già stati caricati correttamente, il server genera un errore.

Il **metodo Play** non rende visibile il carattere. Se il carattere non è visibile, il server riproduce l'animazione in modo invisibile e imposta la [**proprietà Status**](status-property.md) dell'oggetto [**Request.**](/windows/desktop/lwef/the-request-object)

 

 
