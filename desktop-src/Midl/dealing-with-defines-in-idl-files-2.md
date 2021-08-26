---
title: Gestione delle definisce nei file IDL
description: Questa pagina descrive il motivo per cui i simboli definiti con \ define scompaiono dai file H generati dal compilatore MIDL e cosa è possibile fare. Questa spiegazione si applica a tutti i file elaborati da MIDL, ad esempio \ .idl, \ .acf, \ file con estensione h.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL del compilatore MIDL , che si occupa di definisce
- definisce MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c8a63423943d72326b16d53272f63d6efbe7d614661990560b00989be04cf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979702"
---
# <a name="dealing-with-defines-in-idl-files"></a>Gestione \# delle definisce nei file IDL

Questa pagina descrive il motivo **\#** per cui i simboli definiti con una definizione scompaiono dai file H generati dal compilatore MIDL e cosa è possibile fare al riguardo. Questa spiegazione si applica a tutti i file elaborati da MIDL, ad esempio \* idl, \* acf, \* h.

La scomparsa dei **\# simboli di** definizione è il risultato della delega MIDL della pre-elaborazione dei file di input a un preprocessore. Per impostazione predefinita, il preprocessore è un preprocessore C/C++ dell'ambiente di compilazione. Dopo la pre-elaborazione, il flusso di input che MIDL riceve include solo direttive \# per il preprocessore di riga. In particolare, il preprocessore annulla la registrazione di tutte le definizioni di macro nei file di input e pertanto MIDL non è in grado di rilevarne la presenza. Di conseguenza, quando MIDL replica le definizioni dei tipi da un file di input al file H generato, le \# definizioni non vengono replicate. Pertanto, non usare defines direttamente nei file IDL se devono essere usati in un secondo \# momento dal file H generato.

Sono consigliate le quattro soluzioni alternative seguenti:

-   Usare la [**specifica di dichiarazione const.**](const.md)
-   Usare file di intestazione separati importati o inclusi nel file IDL e successivamente inclusi nel codice sorgente C.
-   Usare costanti di enumerazione nel file IDL.
-   Usare [**le \_ virgolette cpp**](cpp-quote.md) per riprodurre **\# define** nel file di intestazione generato.

È possibile riprodurre costanti manifesto usando la **sintassi di dichiarazione di costanti IDL**. Si noti che [**la const**](const.md) nella dichiarazione di costante IDL è diversa dalla semantica **const** C/C++ e introduce semplicemente una costante denominata per una compilazione IDL. Esempio:

``` syntax
const short ARRSIZE = 10
```

Questo esempio specifica che **ARRSIZE** è una costante con valore 10. Le costanti denominate possono essere usate nei dichiaratori di matrici IDL e in altre posizioni in cui un programmatore C userebbe un manifesto definito. Inoltre, questa sintassi comporta la generazione della riga seguente nel file di intestazione:

``` syntax
#define ARRSIZE 10
```

Un altro modo per gestire le istruzioni define è creare un pacchetto in un file di intestazione separato, in un file dedicato alla definizione di istruzioni o in un file che contiene solo definizioni **\#** **\#** di tipo. Un file che contiene solo direttive per il preprocessore può essere incluso in modo sicuro sia dal file IDL che dai file di origine C. Anche se le direttive non saranno disponibili nel file di intestazione generato dal compilatore MIDL, il programma di origine C può includere il file di intestazione separato. In modo analogo, un file di intestazione con istruzioni define e definizioni di tipo normale può essere importato **\#** dal file IDL. Questo approccio incapsula le istruzioni define e typedef usandole in un file H in modo che i simboli di definizione non siano usati direttamente nel file IDL di **\#** **\#** importazione. L'importazione di un file di intestazione o IDL in un altro file IDL impedisce la replica delle istruzioni typedef nel file H generato da MIDL (che è a differenza delle istruzioni **\#** include). Questo approccio consente di fare riferimento in modo sicuro al file di intestazione originale dal codice C lungo il file H generato senza problemi con le definizioni duplicate.

Anche l'uso delle costanti di enumerazione nel file IDL è efficace. Queste costanti possono essere usate nelle espressioni costanti in IDL, ad esempio nei dichiaratori di matrice. Le costanti di enumerazione non vengono rimosse durante le fasi iniziali della compilazione MIDL dal preprocessore del compilatore C, pertanto le costanti di enumerazione sono disponibili nel file di intestazione generato dal compilatore MIDL. Si consideri la seguente istruzione:

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

Questa istruzione non verrà rimossa durante la compilazione MIDL dal preprocessore C e il typedef verrà replicato nel file H generato. La costante MAXSTRINGCOUNT è disponibile per i programmi di origine C che includono il file di intestazione generato dal compilatore MIDL.

Infine, la [**direttiva cpp \_ quote**](cpp-quote.md) di MIDL può essere usata per scrivere una stringa arbitraria direttamente nel file H generato. Ad esempio, per ottenere la costante manifesto usata in precedenza in questa pagina con **\_ virgolette cpp,** è possibile usare l'istruzione seguente:

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

Questa istruzione comporta la generazione della riga seguente nel file di intestazione:

``` syntax
#define ARRSIZE 10
```

 

 




