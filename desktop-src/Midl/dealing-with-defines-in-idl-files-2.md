---
title: Gestione delle definizioni nei file IDL
description: Questa pagina descrive il motivo per cui i simboli definiti con un \ define scompaiono dal compilatore MIDL che ha generato i file H e cosa può essere fatto. Questa spiegazione si applica a tutti i file elaborati da MIDL, ad esempio i file \. idl, \. ACF, \. h.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL compilatore MIDL, gestione delle definizioni
- definisce MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af77979824c2e76352d6f28bef72161249845d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044670"
---
# <a name="dealing-with-defines-in-idl-files"></a>Gestione delle \# definizioni nei file IDL

Questa pagina descrive il motivo per cui i simboli definiti con una **\# definizione** scompaiono dal compilatore MIDL che genera file H e cosa può essere fatto. Questa spiegazione si applica a tutti i file elaborati da MIDL, ad esempio \* i file con estensione IDL, \* ACF e \* h.

La scomparsa dei simboli **\# define** è il risultato della delega della pre-elaborazione dei file di input a un preprocessore. Per impostazione predefinita, il preprocessore è un preprocessore C/C++ dall'ambiente di compilazione. Dopo la pre-elaborazione, il flusso di input MIDL receives ha solo \# direttive per il preprocessore line. In particolare, il preprocessore esegue la registrazione di tutte le definizioni di macro nei file di input e, di conseguenza, MIDL non è in grado di rilevare la loro presenza. Di conseguenza, quando MIDL replica le definizioni dei tipi da un file di input al file H generato, le definizioni \# non vengono replicate. Pertanto, non utilizzare \# le definizioni direttamente nei file idl se devono essere utilizzate in un secondo momento dal file H generato.

Sono consigliate le quattro soluzioni alternative seguenti:

-   Usare la specifica di Dichiarazione [**const**](const.md) .
-   Usare file di intestazione separati che vengono importati o inclusi nel file IDL e successivamente inclusi nel codice sorgente C.
-   Utilizzare le costanti di enumerazione nel file IDL.
-   Usare [**la \_ virgoletta cpp**](cpp-quote.md) per riprodurre la **\# definizione** nel file di intestazione generato.

È possibile riprodurre le costanti manifesto usando la **sintassi della dichiarazione di costanti IDL**. Si noti che il [**const**](const.md) nella dichiarazione di costante IDL è diverso dalla semantica **const** C/C++ e introduce semplicemente una costante denominata per una compilazione IDL. Ad esempio:

``` syntax
const short ARRSIZE = 10
```

Questo esempio specifica che **ARRSIZE** è una costante con valore 10. Le costanti denominate possono essere usate nei dichiaratori di matrici IDL e in altre posizioni in cui un programmatore C userà un manifesto definito. Questa sintassi comporta inoltre la generazione della riga seguente nel file di intestazione:

``` syntax
#define ARRSIZE 10
```

Un altro modo per gestire **\#** le istruzioni define consiste nel creare un pacchetto in un file di intestazione separato, in un file dedicato per la **\#** definizione di istruzioni o in un file che contiene solo definizioni di tipi. Un file che contiene solo le direttive per il preprocessore può essere incluso in modo sicuro sia dal file IDL che dai file di origine C. Sebbene le direttive non saranno disponibili nel file di intestazione generato dal compilatore MIDL, il programma C-Source può includere il file di intestazione separato. Analogamente, un file di intestazione con **\#** istruzioni define e definizioni di tipo regolare può essere importato dal file IDL. Questo approccio incapsula le **\#** istruzioni define e typedef usandole in un file H in modo che i **\#** simboli define non vengano usati direttamente nel file IDL di importazione. L'importazione di un'intestazione o di un file IDL in un altro file IDL impedisce che le istruzioni typedef vengano replicate nel file H generato da MIDL (a differenza delle **\#** istruzioni di inclusione). Questo approccio consente al file di intestazione originale di farvi riferimento in modo sicuro dal codice C lungo il file H generato senza problemi con le definizioni duplicate.

Anche l'utilizzo di costanti di enumerazione nel file IDL è efficace. Queste costanti possono essere utilizzate nelle espressioni costanti in IDL, ad esempio nei dichiaratori di matrice. Le costanti di enumerazione non vengono rimosse durante le fasi iniziali della compilazione MIDL da parte del preprocessore del compilatore C, quindi le costanti di enumerazione sono disponibili nel file di intestazione generato dal compilatore MIDL. Si consideri la seguente istruzione:

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

Questa istruzione non verrà rimossa durante la compilazione MIDL da parte del preprocessore C e il typedef verrà replicato nel file H generato. La costante MAXSTRINGCOUNT è disponibile per i programmi di origine C che includono il file di intestazione generato dal compilatore MIDL.

Infine, è possibile usare la direttiva per le [**\_ virgolette cpp**](cpp-quote.md) di MIDL per scrivere una stringa arbitraria direttamente nel file H generato. Per ottenere, ad esempio, la costante del manifesto utilizzata in precedenza in questa pagina con **\_ virgolette cpp**, è possibile utilizzare l'istruzione seguente:

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

Questa istruzione determina la generazione della riga seguente nel file di intestazione:

``` syntax
#define ARRSIZE 10
```

 

 




