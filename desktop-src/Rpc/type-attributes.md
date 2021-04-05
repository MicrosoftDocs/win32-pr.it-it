---
title: Attributi di tipo
description: Remote Procedure Call (RPC) e gli attributi di tipo MIDL che possono essere applicati alle dichiarazioni di tipo.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378fbc91f17e77baff7e259bd3551a47fde653cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872549"
---
# <a name="type-attributes"></a>Attributi di tipo

Gli attributi di tipo sono gli attributi MIDL che è possibile applicare alle dichiarazioni di tipo:

-   **\[**[**gestire**](/windows/desktop/Midl/handle)**\]**
-   **\[**[**handle di contesto \_**](/windows/desktop/Midl/context-handle)**\]**
-   **\[**[**tipo di opzione \_**](/windows/desktop/Midl/switch-type)**\]**
-   [attributi di tipo puntatore](three-pointer-types.md)

L'attributo **\[ Switch \_ Type \]** designa il tipo di un discriminatore di Unione. Questo attributo si applica solo a un'Unione non incapsulata.

Un handle di contesto è un puntatore con un attributo dell' **\[ \_ handle \] di contesto** . L'attributo **\[ \_ handle \] di contesto** consente di scrivere procedure per la gestione delle informazioni sullo stato tra le chiamate a procedure remote. Un handle di contesto con un valore non null rappresenta il contesto salvato e serve due scopi:

-   Sul lato client, contiene le informazioni richieste dalla libreria di runtime RPC per indirizzare la chiamata al server.
-   Sul lato server, funge da handle nel contesto attivo.

L' **\[** [](/windows/desktop/Midl/handle) **\]** attributo handle specifica che un tipo può verificarsi come handle definito dall'utente (generico). Questa funzionalità consente la progettazione di handle significativi per l'applicazione. L'utente deve fornire routine di binding e di annullamento dell'associazione per eseguire la conversione tra il tipo di handle definito dall'utente e il tipo di handle della primitiva RPC, **handle \_ t**. Un handle primitivo contiene informazioni sulla destinazione significative per le librerie di runtime RPC. Un handle definito dall'utente può essere definito solo in una dichiarazione di tipo, non in una dichiarazione di funzione. Un parametro con l'attributo **\[ handle \]** ha un doppio scopo. Viene utilizzato per determinare il binding per la chiamata e viene trasmesso alla routine chiamata come parametro dati normale.

 

 