---
title: Eventi secondari
description: Eventi secondari
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Windows Media Player, eventi secondari
- interfaccia, eventi secondari
- eventi, secondario
- scrittura di codice per le interfaccia, eventi secondari
- eventi secondari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fd121330a99c73ed7a52def712bb53949113745a8af0f4c01ded8f9aeaea4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735781"
---
# <a name="secondary-events"></a>Eventi secondari

È possibile determinare quali altri eventi si verificano quando viene attivato un evento specifico. Ad esempio, quando si fa clic su un pulsante del mouse, è possibile sapere se il tasto ALT era premuto contemporaneamente.

## <a name="event-attributes"></a>Attributi dell'evento

Per le interfaccia sono supportati gli attributi degli eventi seguenti:

-   **altKey**
-   **Pulsante**
-   **clientX**
-   **clientY**
-   **CTRLKEY**
-   **fromElement**
-   **offsetX**
-   **Offsety**
-   **screenX**
-   **screenY**
-   **maiuscKey**
-   **srcElement**
-   **toElement**
-   **x**
-   **y**
-   **Keycode**

Per altre informazioni su questi attributi, vedere Le informazioni [di riferimento sulla programmazione dell'interfaccia](skin-programming-reference.md).

## <a name="using-secondary-events"></a>Uso di eventi secondari

È possibile elaborare solo gli attributi degli eventi JScript codice. È necessario usare la sintassi seguente:


```C++
event.eventattributename
```



*eventattributename è* il nome dell'attributo dell'evento. Ad esempio, per determinare se il tasto ALT è stato premuto durante un evento Click, è possibile usare le righe seguenti nel JScript seguente:


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

 

 




