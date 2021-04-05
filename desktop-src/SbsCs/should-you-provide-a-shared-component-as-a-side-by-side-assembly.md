---
description: Se uno o più dei seguenti casi sono veri, i provider di componenti condivisi dovrebbero considerare la possibilità di rendere disponibile il componente come assembly side-by-side.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: È necessario fornire un componente condiviso come assembly affiancato?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733adf400ba9ce019d9f749fcd79a1a71380c9e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884526"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a>È necessario fornire un componente condiviso come assembly affiancato?

Per i provider di componenti condivisi è consigliabile rendere disponibile il componente come assembly affiancato se si verificano una o più delle condizioni seguenti:

-   Il componente espone un Application Programming Interface completo utilizzato da molte applicazioni. Ad esempio, un componente come MSHTML, che consente alle applicazioni C e C++ di accedere al modello a oggetti DHTML (Dynamic HTML).
-   Il componente è già condiviso da più applicazioni. Ad esempio, un componente come COMCTL32, che consente alle applicazioni di accedere ai controlli comuni.
-   Il componente è un nuovo componente.
-   Il componente è un componente in modalità utente e non un driver di dispositivo.

Non tutti i componenti sono un candidato adatto per un assembly affiancato. Un componente non è un candidato adatto per un assembly affiancato se si verifica una delle condizioni seguenti:

-   Il componente gestisce la comunicazione tra le applicazioni. Ad esempio, parti di OLE32 non rendono un assembly side-by-side efficace perché non si vogliono avere due versioni diverse delle parti che coordinano la comunicazione tra le applicazioni eseguite nel sistema.
-   Il componente gestisce un dispositivo fisico o virtuale per il sistema. Ad esempio un driver di dispositivo per uno spooler di stampa.

In alcuni casi potrebbe essere possibile per lo sviluppatore del componente riprogettare un componente esistente per renderlo idoneo per la pubblicazione come assembly affiancato. Per ulteriori informazioni, vedere [linee guida per la creazione di assembly affiancati](guidelines-for-creating-side-by-side-assemblies.md).

 

 



