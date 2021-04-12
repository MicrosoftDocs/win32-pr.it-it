---
title: Eventi secondari
description: Eventi secondari
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Windows Media Player Skin, eventi secondari
- interfacce, eventi secondari
- eventi, secondari
- scrittura di codice per interfacce, eventi secondari
- eventi secondari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e04785a7468353665083287ac1b74bce5cbf0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471595"
---
# <a name="secondary-events"></a>Eventi secondari

È possibile determinare gli altri eventi che avvengono quando viene attivato un evento specifico. Ad esempio, quando si fa clic su un pulsante del mouse, è possibile che si desideri sapere se il tasto ALT è stato disattivato nello stesso momento.

## <a name="event-attributes"></a>Attributi dell'evento

Per le interfacce sono supportati gli attributi di evento seguenti:

-   **altKey**
-   **pulsante**
-   **clientX**
-   **clientY**
-   **ctrlKey**
-   **fromElement**
-   **offsetX**
-   **offsetY**
-   **screenX**
-   **screenY**
-   **shiftKey**
-   **srcElement**
-   **toElement**
-   **x**
-   **y**
-   **keyCode**

Per ulteriori informazioni su questi attributi, vedere la Guida di riferimento per la [programmazione dell'interfaccia](skin-programming-reference.md).

## <a name="using-secondary-events"></a>Uso di eventi secondari

È possibile elaborare solo gli attributi di evento nel codice JScript. È necessario utilizzare la sintassi seguente:


```C++
event.eventattributename
```



*eventattributename* è il nome dell'attributo dell'evento. Per determinare, ad esempio, se il tasto ALT è stato premuto durante un evento di clic, è possibile utilizzare le righe seguenti nel codice JScript:


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione degli eventi**](handling-events.md)
</dt> </dl>

 

 




