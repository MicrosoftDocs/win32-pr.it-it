---
title: Abilitazione di STRICT
description: Quando si definisce il simbolo STRICT, si abilitano le funzionalità che richiedono maggiore attenzione nella dichiarazione e nell'utilizzo dei tipi.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0400b67025f11dc9c58553f6835b2a8e2b36b4c
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "106320251"
---
# <a name="enabling-strict"></a>Abilitazione di STRICT

Quando si definisce il simbolo **strict** , si abilitano le funzionalità che richiedono maggiore attenzione nella dichiarazione e nell'utilizzo dei tipi. Questo consente di scrivere codice più portatile. Questa ulteriore attenzione ridurrà anche il tempo di debug. L'abilitazione di **strict** ridefinisce determinati tipi di dati in modo che il compilatore non consenta l'assegnazione da un tipo a un altro senza un cast esplicito. Questa operazione è particolarmente utile per il codice di Windows. Gli errori nel passaggio dei tipi di dati vengono segnalati in fase di compilazione anziché causare errori irreversibili in fase di esecuzione.

Con Visual C++, il controllo dei tipi **strict** è definito per impostazione predefinita.

Per definire **strict** in base a file, inserire un'istruzione **\# define** prima di includere Windows. h:


```C++
#define STRICT
#include <windows.h>
```



Quando è definito **strict** , le definizioni [dei tipi di dati](windows-data-types.md) cambiano come segue:

-   I tipi di handle specifici vengono definiti per escludersi a vicenda. ad esempio, non sarà possibile passare un **HWND** in cui è richiesto un argomento di tipo **HDC** . Senza **strict**, tutti gli handle sono definiti come **handle**, pertanto il compilatore non impedisce l'uso di un tipo di handle in cui è previsto un altro tipo.
-   Tutti i tipi di funzione di callback, ad esempio le routine della finestra di dialogo, le routine della finestra e le routine hook, sono definiti con prototipi completi. In questo modo si impedisce la dichiarazione di funzioni di callback con elenchi di parametri non corretti.
-   I tipi di parametro e valore restituito che devono usare un puntatore generico sono dichiarati correttamente come **LPVOID** anziché come **LPSTR** o un altro tipo di puntatore.
-   La struttura [**Comstat**](/windows/desktop/api/winbase/ns-winbase-comstat) viene dichiarata in base allo standard ANSI.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Disabilitazione di STRICT](disabling-strict.md)
</dt> <dt>

[Conformità RIGOROSa](strict-compliance.md)
</dt> </dl>

 

 
