---
title: Handle impliciti e espliciti
description: Per dichiarare un handle di serializzazione, usare il tipo di handle primitivo handle \_ t.
ms.assetid: 70d8665f-d793-46fc-bcbf-ecb24e746786
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcead663ae7eee8d0cdb95a73e7ae58935773cef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872842"
---
# <a name="implicit-vs-explicit-handles"></a>Handle impliciti e espliciti

Per dichiarare un handle di serializzazione, usare il tipo di handle primitivo [**handle \_ t**](/windows/desktop/Midl/handle-t). Gli handle di serializzazione possono essere espliciti o impliciti. Specificare gli handle impliciti nell'ACF dell'applicazione usando l'attributo **\[ \_ handle \] implicito** . Il compilatore MIDL genererà una variabile globale dell'handle di serializzazione. Le procedure di serializzazione con un handle implicito utilizzano questa variabile globale per accedere a un contesto di serializzazione valido.

Quando si utilizza la codifica dei tipi, le routine generate che supportano la serializzazione di un particolare tipo utilizzano l'handle implicito globale per accedere al contesto di serializzazione. Si noti che le routine remote possono richiedere l'uso dell'handle implicito come handle di binding. Verificare che l'handle implicito sia impostato su un handle di serializzazione valido prima di effettuare una chiamata di serializzazione.

Un handle esplicito viene specificato come parametro del prototipo della procedura di serializzazione nel file IDL oppure può essere specificato anche usando l'attributo **\[ \_ handle \] esplicito** in ACF. Il parametro dell'handle esplicito viene utilizzato per stabilire il contesto di serializzazione appropriato per la procedura. Per stabilire il contesto corretto nel caso della serializzazione dei tipi, il compilatore genera le routine di supporto che usano il parametro esplicito [**handle \_ t**](/windows/desktop/Midl/handle-t) come handle di serializzazione. È necessario fornire un handle di serializzazione valido quando si chiama una routine di serializzazione o una routine di supporto del tipo di serializzazione.

 

 