---
title: Handle impliciti o espliciti
description: Per dichiarare un handle di serializzazione, usare l'handle di tipo handle primitivo \_ t.
ms.assetid: 70d8665f-d793-46fc-bcbf-ecb24e746786
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9f6dabc8a6e4d0e5ccac7ac8b94e1812d81a674b471015c868b32209fd9746
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020461"
---
# <a name="implicit-vs-explicit-handles"></a>Handle impliciti o espliciti

Per dichiarare un handle di serializzazione, usare l'handle di tipo handle [**primitivo \_ t**](/windows/desktop/Midl/handle-t). Gli handle di serializzazione possono essere espliciti o impliciti. Specificare handle impliciti nel file ACF dell'applicazione usando **\[ \_ l'attributo handle \] implicito.** Il compilatore MIDL genererà una variabile di handle di serializzazione globale. Le procedure di serializzazione con un handle implicito usano questa variabile globale per accedere a un contesto di serializzazione valido.

Quando si usa la codifica dei tipi, le routine generate che supportano la serializzazione di un determinato tipo usano l'handle implicito globale per accedere al contesto di serializzazione. Si noti che le routine remote potrebbero dover usare l'handle implicito come handle di associazione. Assicurarsi che l'handle implicito sia impostato su un handle di serializzazione valido prima di eseguire una chiamata di serializzazione.

Un handle esplicito viene specificato come parametro del prototipo della procedura di serializzazione nel file IDL oppure può essere specificato anche usando l'attributo **\[ \_ handle \]** esplicito in ACF. Il parametro handle esplicito viene usato per stabilire il contesto di serializzazione appropriato per la procedura. Per stabilire il contesto corretto nel caso della serializzazione del tipo, il compilatore genera le routine di supporto che usano il parametro [**\_ t dell'handle**](/windows/desktop/Midl/handle-t) esplicito come handle di serializzazione. È necessario fornire un handle di serializzazione valido quando si chiama una routine di serializzazione o una routine di supporto del tipo di serializzazione.

 

 