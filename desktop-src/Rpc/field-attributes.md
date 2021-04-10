---
title: Attributi di campo
description: Attributi di campo (attributi applicati ai campi di una matrice, una struttura, un'Unione o una matrice di caratteri) e RPC (Remote Procedure Call).
ms.assetid: 4508479d-ff0a-4698-94aa-588837032067
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b9421ddf4ea7e7bc4c70af0ecd826e2681875d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963396"
---
# <a name="field-attributes"></a>Attributi di campo

Gli attributi di campo sono gli attributi che possono essere applicati ai campi di una matrice, una struttura, un'Unione o una matrice di caratteri:

-   **\[**[**Ignora**](/windows/desktop/Midl/ignore) **\]** , **\[** [ **dimensioni \_** :](/windows/desktop/Midl/size-is)**\]**
-   **\[**[**Max \_ è**](/windows/desktop/Midl/max-is)**\]**
-   **\[**[**lunghezza \_**](/windows/desktop/Midl/length-is)**\]**
-   **\[**[**il primo \_ è**](/windows/desktop/Midl/first-is)**\]**
-   **\[**[**ultimo \_ è**](/windows/desktop/Midl/last-is)**\]**
-   **\[**[**opzione \_**](/windows/desktop/Midl/switch-is)**\]**
-   **\[**[**stringa**](/windows/desktop/Midl/string)**\]**
-   [attributi puntatore](three-pointer-types.md)

Gli attributi di campo, ad esempio, vengono utilizzati in combinazione con le dichiarazioni di matrice per specificare la dimensione della matrice o la parte della matrice che contiene dati validi. Questa operazione viene eseguita associando un altro parametro, il campo della struttura o un'espressione costante con la matrice.

L' **\[** attributo [**Ignore**](/windows/desktop/Midl/ignore) **\]** designa i campi puntatore da ignorare durante il processo di marshalling. Tale campo ignorato viene impostato su **null** sul lato ricevitore.

MIDL fornisce matrici *conformi*, *variabili* e *aperte* . Una matrice viene chiamata conforme se i relativi limiti vengono determinati in fase di esecuzione. La **\[** [**dimensione \_ è**](/windows/desktop/Midl/size-is) **\]** attributo che definisce il limite superiore per le dimensioni di allocazione della matrice e l' **\[** attributo [**Max \_ is**](/windows/desktop/Midl/max-is) **\]** designa il limite superiore del valore di un indice di matrice valido. Per ulteriori informazioni, vedere **\[** [**matrici**](arrays.md) **\]** .

Una matrice viene chiamata variabile se i relativi limiti vengono determinati in fase di compilazione, ma l'intervallo di elementi trasmessi viene determinato in fase di esecuzione. Un array aperto, detto anche matrice di variabili conforme, è una matrice il cui limite superiore e l'intervallo di elementi trasmessi vengono determinati in fase di esecuzione. Per determinare l'intervallo di elementi trasmessi di una matrice, la dichiarazione di matrice deve includere una **\[** [**lunghezza \_**](/windows/desktop/Midl/length-is), ovvero l' **\]** **\[** attributo [**First \_ è**](/windows/desktop/Midl/first-is) **\]** o **\[** [**Last \_ è**](/windows/desktop/Midl/last-is) **\]** .

L'attributo **\[ \_ \] length** indica il numero di elementi della matrice da trasmettere e il primo attributo **\[ \_ è \]** che definisce l'indice del primo elemento della matrice da trasmettere. Il **\[ penultimo \_ \]** attributo definisce l'indice dell'ultimo elemento della matrice da trasmettere.

L' **\[** [**opzione \_ è**](/windows/desktop/Midl/switch-is) **\]** attributo campo designa un discriminatore di Unione. Quando l'Unione è un parametro di routine, il discriminatore di Unione deve essere un altro parametro della stessa routine. Quando l'Unione è un campo di una struttura, il discriminatore deve essere un altro campo della struttura allo stesso livello del campo di Unione. Il discriminatore deve essere un tipo [**booleano**](/windows/desktop/Midl/boolean), [**char**](/windows/desktop/Midl/char-idl), [**int**](/windows/desktop/Midl/int)o [**enum**](/windows/desktop/Midl/enum) oppure un tipo che si risolve in uno di questi tipi. Per ulteriori informazioni, vedere unioni e **\[ Switch \_ \]** non [incapsulati](/windows/desktop/Midl/nonencapsulated-unions) .

L' **\[** [](/windows/desktop/Midl/string) **\]** attributo di campo stringa indica che una matrice di byte o caratteri unidimensionali o un puntatore a un carattere o a un flusso di byte con terminazione zero deve essere considerato come una stringa. L'attributo stringa si applica solo a matrici e puntatori unidimensionali. Il tipo di elemento è limitato a [**char**](/windows/desktop/Midl/char-idl), [**byte**](/windows/desktop/Midl/byte), [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t)o a un tipo denominato che viene risolto in uno di questi tipi.

Per informazioni sul contesto in cui vengono visualizzati gli attributi di campo, vedere [matrici MIDL](/windows/desktop/Midl/midl-arrays), [strutture MIDL](/windows/desktop/Midl/midl-structures)e [unioni MIDL](/windows/desktop/Midl/midl-unions).

 

 