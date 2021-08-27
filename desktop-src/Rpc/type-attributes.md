---
title: Attributi di tipo
description: Remote Procedure Call (RPC) e gli attributi di tipo MIDL che possono essere applicati alle dichiarazioni di tipo.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5da8f3beb62f443b95a42283d4625200812436bce1bc667edc07d68f2542544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011169"
---
# <a name="type-attributes"></a>Attributi di tipo

Gli attributi di tipo sono gli attributi MIDL che possono essere applicati alle dichiarazioni di tipo:

-   **\[**[**Gestire**](/windows/desktop/Midl/handle)**\]**
-   **\[**[**handle di \_ contesto**](/windows/desktop/Midl/context-handle)**\]**
-   **\[**[**tipo di \_ commutatore**](/windows/desktop/Midl/switch-type)**\]**
-   [Attributi del tipo di puntatore](three-pointer-types.md)

**\[ L'attributo switch \_ type \]** definisce il tipo di un discriminatore di unione. Questo attributo si applica solo a un'unione non incapsulata.

Un handle di contesto è un puntatore con un **\[ attributo di handle \_ di \]** contesto. **\[ L'attributo di \_ handle \]** di contesto consente di scrivere procedure che mantengono le informazioni sullo stato tra le chiamate di procedura remota. Un handle di contesto con un valore non Null rappresenta il contesto salvato e svolge due scopi:

-   Sul lato client contiene le informazioni necessarie alla libreria di runtime RPC per indirizzare la chiamata al server.
-   Sul lato server, funge da handle nel contesto attivo.

**\[** [**L'attributo**](/windows/desktop/Midl/handle) handle specifica che un tipo può verificarsi come handle **\]** definito dall'utente (generico). Questa funzionalità consente la progettazione di handle significativi per l'applicazione. L'utente deve fornire routine di associazione e annullamento dell'associazione per eseguire la conversione tra il tipo di handle definito dall'utente e il tipo di handle primitivo RPC, **\_ gestire t**. Un handle primitivo contiene informazioni di destinazione significative per le librerie di runtime RPC. Un handle definito dall'utente può essere definito solo in una dichiarazione di tipo, non in una dichiarazione di funzione. Un parametro con **\[ l'attributo handle \]** ha un doppio scopo. Viene usato per determinare l'associazione per la chiamata e viene trasmesso alla routine chiamata come parametro di dati normale.

 

 