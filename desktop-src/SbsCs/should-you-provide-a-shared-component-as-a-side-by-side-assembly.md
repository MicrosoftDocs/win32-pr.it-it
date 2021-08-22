---
description: I provider di componenti condivisi devono prendere in considerazione la possibilità di rendere disponibile il componente come assembly side-by-side se si verifica uno o più dei casi seguenti.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: È necessario fornire un componente condiviso come assembly side-by-side?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92dbd205db37c769050614c60ce4cc3637b27be9108f25b3c1c8f553851df82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141894"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a>È necessario fornire un componente condiviso come assembly side-by-side?

I provider di componenti condivisi devono prendere in considerazione la possibilità di rendere disponibile il componente come assembly side-by-side se uno o più degli elementi seguenti sono veri:

-   Il componente espone un'interfaccia di programmazione di applicazioni ricca usata da molte applicazioni. Ad esempio, un componente come MSHTML, che consente alle applicazioni C e C++ di accedere al modello a oggetti DHTML (Dynamic HTML).
-   Il componente è già condiviso da più applicazioni. Ad esempio, un componente come COMCTL32, che fornisce alle applicazioni l'accesso ai controlli comuni.
-   Il componente è un nuovo componente.
-   Il componente è un componente in modalità utente e non un driver di dispositivo.

Non tutti i componenti sono idonei per un assembly side-by-side. Un componente non è un candidato adatto per un assembly side-by-side se si verifica una delle condizioni seguenti:

-   Il componente gestisce la comunicazione tra le applicazioni. Ad esempio, parti di OLE32 non costituiscono un assembly side-by-side valido perché non si vogliono avere due versioni diverse delle parti che coordinano la comunicazione tra le applicazioni eseguite nel sistema.
-   Il componente gestisce un dispositivo fisico o virtuale per il sistema. Ad esempio, un driver di dispositivo per uno spooler di stampa.

In alcuni casi può essere possibile per lo sviluppatore del componente riprogettare un componente esistente per renderlo adatto per la pubblicazione come assembly side-by-side. Per altre informazioni, [vedere Linee guida per la creazione di assembly side-by-side.](guidelines-for-creating-side-by-side-assemblies.md)

 

 



