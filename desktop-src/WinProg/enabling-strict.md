---
title: Abilitazione di STRICT
description: Quando si definisce il simbolo STRICT, si abilitano le funzionalità che richiedono maggiore attenzione nella dichiarazione e nell'uso dei tipi.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca6ca814d69910620b89095cc18be3b37601329dc053937d5772243097537c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561795"
---
# <a name="enabling-strict"></a>Abilitazione di STRICT

Quando si definisce il **simbolo STRICT,** si abilitano le funzionalità che richiedono maggiore attenzione nella dichiarazione e nell'uso dei tipi. Ciò consente di scrivere codice più portabile. Questa attenzione aggiuntiva ridurrà anche il tempo di debug. **L'abilitazione** di STRICT ridefinisce determinati tipi di dati in modo che il compilatore non consenta l'assegnazione da un tipo a un altro senza un cast esplicito. Ciò è particolarmente utile con Windows codice. Gli errori durante il passaggio dei tipi di dati vengono segnalati in fase di compilazione anziché causare errori irreversibili in fase di esecuzione.

Con Visual C++, **il controllo dei** tipi STRICT è definito per impostazione predefinita.

Per definire **STRICT** file per file, inserire un'istruzione **\# define** prima di includere Windows.h:


```C++
#define STRICT
#include <windows.h>
```



Quando **viene definito STRICT,** le [definizioni dei tipi di](windows-data-types.md) dati cambiano nel modo seguente:

-   I tipi di handle specifici vengono definiti in modo che si escludono a vicenda. Ad esempio, non sarà possibile passare un **HWND** in cui è necessario un argomento di tipo **HDC.** Senza **STRICT,** tutti gli handle sono definiti come **HANDLE,** quindi il compilatore non impedisce di usare un tipo di handle in cui è previsto un altro tipo.
-   Tutti i tipi di funzione di callback, ad esempio le routine di finestra di dialogo, le routine finestra e le routine hook, vengono definiti con prototipi completi. Ciò impedisce di dichiarare funzioni di callback con elenchi di parametri non corretti.
-   I tipi parametro e valore restituito che devono usare un puntatore generico vengono dichiarati correttamente come **LPVOID** anziché **come LPSTR** o un altro tipo di puntatore.
-   La [**struttura COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) viene dichiarata in base agli standard ANSI.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Disabilitazione di STRICT](disabling-strict.md)
</dt> <dt>

[Conformità STRICT](strict-compliance.md)
</dt> </dl>

 

 
