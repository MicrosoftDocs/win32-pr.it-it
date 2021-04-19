---
title: Metodo Play (funzionalità legacy dell'ambiente Windows)
description: Metodo Play
ms.assetid: 7e89341a-b4d3-4bea-8e7f-31c649ff06b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d06f4275d7b4c0959a59536c8b20a95c14ab1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300743"
---
# <a name="play-method-legacy-windows-environment-features"></a>Metodo Play (funzionalità legacy dell'ambiente Windows)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Riproduce l'animazione specificata per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("**_CharacterID_*_"). Riproduci_* "*animationName*"

</dd> </dl> 

| Parte            | Descrizione                                                          |
|-----------------|----------------------------------------------------------------------|
| *AnimationName* | Obbligatorio. Stringa che specifica il nome di una sequenza di animazione. |



 

## <a name="remarks"></a>Commenti

Il nome di un'animazione viene definito quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent. Prima di riprodurre l'animazione specificata, il server tenta di riprodurre l'animazione **restituita** per l'animazione precedente, se ne è stata assegnata una.

Quando si accede alle animazioni di un carattere usando un protocollo file convenzionale, è possibile usare semplicemente il metodo **Play** specificando il nome dell'animazione. Tuttavia, se si utilizza il protocollo HTTP per accedere ai dati di animazione dei caratteri, utilizzare il metodo **Get** per caricare l'animazione prima di chiamare il metodo **Play** .

Per ulteriori informazioni, vedere il metodo **Get** .

Per semplificare la sintassi, è possibile dichiarare un riferimento a un oggetto e impostarlo in modo che faccia riferimento all'oggetto [**character**](/windows/desktop/lwef/the-characters-object) nella raccolta [**characters**](/windows/desktop/lwef/the-characters-object) e usare il riferimento come parte delle istruzioni **Play** :


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



Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) . Inoltre, se si specifica un'animazione che non viene caricata o se il carattere non è stato caricato correttamente, il server imposta la proprietà [**status**](status-property.md) dell'oggetto **Request** su "failed" con un numero di errore appropriato. Tuttavia, se l'animazione non esiste e i dati del carattere sono già stati caricati correttamente, il server genera un errore.

Il metodo **Play** non rende visibile il carattere. Se il carattere non è visibile, il server riproduce l'animazione in maniera invisibile e imposta la proprietà [**status**](status-property.md) dell'oggetto [**Request**](/windows/desktop/lwef/the-request-object) .

 

 
