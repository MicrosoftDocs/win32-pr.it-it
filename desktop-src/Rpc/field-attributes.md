---
title: Attributi di campo
description: Attributi di campo (attributi applicati ai campi di una matrice, struttura, unione o matrice di caratteri) e RPC (Remote Procedure Call).
ms.assetid: 4508479d-ff0a-4698-94aa-588837032067
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6d14bab0cf14710e91fceb466111c4af32d3d2828e4b7bdacc9494fa27b7d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930000"
---
# <a name="field-attributes"></a>Attributi di campo

Gli attributi di campo sono gli attributi che possono essere applicati ai campi di una matrice, struttura, unione o matrice di caratteri:

-   **\[**[**ignore**](/windows/desktop/Midl/ignore) **\]** , size **\[** [ **\_ è**](/windows/desktop/Midl/size-is)**\]**
-   **\[**[**max \_ is**](/windows/desktop/Midl/max-is)**\]**
-   **\[**[**length \_ è**](/windows/desktop/Midl/length-is)**\]**
-   **\[**[**first \_ è**](/windows/desktop/Midl/first-is)**\]**
-   **\[**[**last \_ is**](/windows/desktop/Midl/last-is)**\]**
-   **\[**[**\_l'opzione è**](/windows/desktop/Midl/switch-is)**\]**
-   **\[**[**Stringa**](/windows/desktop/Midl/string)**\]**
-   [Attributi puntatore](three-pointer-types.md)

Ad esempio, gli attributi di campo vengono usati insieme alle dichiarazioni di matrice per specificare le dimensioni della matrice o la parte della matrice che contiene dati validi. Questa operazione viene eseguita associando un altro parametro, un campo di struttura o un'espressione costante alla matrice.

**\[** [**L'attributo ignore**](/windows/desktop/Midl/ignore) **\]** definisce i campi puntatore da ignorare durante il processo di marshalling. Tale campo ignorato è impostato su **NULL** sul lato ricevitore.

MIDL fornisce *matrici aperte* *,* variabili *e* conformi. Una matrice viene chiamata conforme se i limiti vengono determinati in fase di esecuzione. L'attributo size indica il limite superiore per le dimensioni di allocazione della matrice e l'attributo max is definisce il limite superiore sul valore di un indice di **\[** [**\_**](/windows/desktop/Midl/size-is) **\]** matrice **\[** [**\_**](/windows/desktop/Midl/max-is) **\]** valido. Per altre informazioni, vedere **\[** [**matrici**](arrays.md) **\]** .

Una matrice viene chiamata variabile se i limiti vengono determinati in fase di compilazione, ma l'intervallo di elementi trasmessi viene determinato in fase di esecuzione. Una matrice aperta (detta anche matrice variabile conforme) è una matrice il cui limite superiore e l'intervallo di elementi trasmessi vengono determinati in fase di esecuzione. Per determinare l'intervallo di elementi trasmessi di una matrice, la dichiarazione di matrice deve includere una lunghezza , la prima è **\[** [**\_**](/windows/desktop/Midl/length-is) **\]** o **\[** [**\_**](/windows/desktop/Midl/first-is) **\]** **\[** [**\_ l'ultima è l'attributo**](/windows/desktop/Midl/last-is) **\]** .

**\[ L'attributo \_ length \]** indica il **\[ \_ \]** numero di elementi della matrice da trasmettere e il primo è l'attributo che definisce l'indice del primo elemento della matrice da trasmettere. **\[ \_ L'ultimo \] attributo** è che definisce l'indice dell'ultimo elemento della matrice da trasmettere.

**\[** [**L'opzione è \_ un**](/windows/desktop/Midl/switch-is) **\]** attributo di campo che definisce un discriminatore di unione. Quando l'unione è un parametro di routine, il discriminatore di unione deve essere un altro parametro della stessa procedura. Quando l'unione è un campo di una struttura, il discriminatore deve essere un altro campo della struttura allo stesso livello del campo di unione. Il discriminatore deve essere [**un tipo booleano**](/windows/desktop/Midl/boolean), [**char**](/windows/desktop/Midl/char-idl), [**int**](/windows/desktop/Midl/int)o [**enum**](/windows/desktop/Midl/enum) oppure un tipo che viene risolto in uno di questi tipi. Per altre informazioni, vedere [Unioni non](/windows/desktop/Midl/nonencapsulated-unions) incapsulate e **\[ l'opzione \_ è \]**.

L'attributo del campo stringa indica che un carattere unidimensionale o una matrice di byte o un puntatore a un flusso di byte o un carattere con terminazione zero deve essere **\[** [](/windows/desktop/Midl/string) **\]** considerato come una stringa. L'attributo stringa si applica solo a matrici e puntatori unidimensionali. Il tipo di elemento è limitato a [**char**](/windows/desktop/Midl/char-idl), [**byte**](/windows/desktop/Midl/byte), [**wchar \_ t**](/windows/desktop/Midl/wchar-t)o a un tipo denominato che viene risolto in uno di questi tipi.

Per informazioni sul contesto in cui vengono visualizzati gli attributi di campo, vedere [Matrici MIDL,](/windows/desktop/Midl/midl-arrays)strutture [MIDL](/windows/desktop/Midl/midl-structures)e [unioni MIDL.](/windows/desktop/Midl/midl-unions)

 

 