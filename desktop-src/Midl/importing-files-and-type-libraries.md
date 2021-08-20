---
title: Importazione di file e librerie dei tipi
description: Le parole chiave MIDL includono, importano e importlib consentono di riutilizzare il codice facendo riferimento ai file di intestazione, IDL e ODL (Object Definition Language) esistenti e alle librerie dei tipi compilate.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Microsoft Interface Definition Language MIDL, attività, importazione di file e librerie dei tipi
- importazione di MIDL
- librerie dei tipi MIDL , importazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099ada5122ad024e342148bf3c453df0bd50872e6d59a2bbabd7d2892af5f93a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013739"
---
# <a name="importing-files-and-type-libraries"></a>Importazione di file e librerie dei tipi

Le parole chiave MIDL includono [**,**](include.md) [**import**](import.md)e [**importlib**](importlib.md) consentono di riutilizzare il codice facendo riferimento a file di intestazione, IDL e ODL (Object Definition Language) esistenti e librerie dei tipi compilate.

La direttiva [**include**](include.md) ACF consente di specificare in un file ACF uno o più file di intestazione del linguaggio C da includere nel codice stub generato da MIDL. Il file generato avrà una riga con una direttiva **\# include** del preprocessore C con il file di intestazione indicato. Usare questa **direttiva include** per inserire i file di intestazione specifici di un particolare ambiente operativo e che non contengono le informazioni necessarie per l'interfaccia tra client e server. Non usare **include per** i file di intestazione contenenti i tipi di dati che si desidera sia disponibile per il file IDL. usare invece la [**direttiva import.**](import.md)

## <a name="example-1"></a>Esempio 1

``` syntax
[
  auto_handle
] 
interface X86PC
{ 
  include "gendefs.h", "protos.h", "myfile.h"; 
  //interface typdefs and function declarations here
}
```

La direttiva [**import**](import.md) IDL è il metodo standard per l'importazione di definizioni di tipi e interfacce da altri file IDL (o ODL) e file di intestazione nel file IDL. Tutte le istruzioni IDL nel file importato, ad esempio typedef, [**dichiarazioni const**](const.md) e definizioni di interfaccia, diventano disponibili per il file IDL di importazione.

Analogamente alla direttiva per il preprocessore del linguaggio C **\# include**, la direttiva [**import**](import.md) indica al compilatore di includere i tipi di dati definiti nei file IDL importati. A differenza **\# della direttiva include,** la **direttiva import** ignora i prototipi di procedura, poiché non vengono generati stub per qualsiasi elemento nel file importato. Poiché il preprocessore viene richiamato separatamente per il file importato, le direttive del preprocessore (ad esempio **) non vengono trasportate nel file IDL di importazione.

Per altre informazioni sull'uso di [**import**](import.md) per includere i file di intestazione di sistema in un file IDL, vedere [Importing System Header Files](importing-system-header-files.md).

## <a name="example-2"></a>Esempio 2

``` syntax
[
  uuid(. . .), object
] 
interface IKnown : IUnknown
{
  import "base.idl", "unknwn.idl", "helper.idl";
  //remainder of interface definition
}
```

La direttiva [**importlib**](importlib.md) ODL consente di fare riferimento a una libreria dei tipi compilata nel file IDL o ODL. La **direttiva importlib** deve essere all'interno di [**un'istruzione library**](library.md) e deve precedere altre descrizioni dei tipi nella libreria. La libreria importata, nonché la libreria generata, devono essere disponibili per l'applicazione in fase di esecuzione.

## <a name="example-3"></a>Esempio 3

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

È anche possibile usare la direttiva include del **\# preprocessore** C per includere intestazioni e altri file nel file IDL o ODL. Tenere presente, tuttavia, che questa direttiva includerà letteralmente l'intero contenuto del file specificato. Se un file di intestazione contiene prototipi non necessari o desiderati nei file stub generati da MIDL o se contiene definizioni di tipo nonremobili, è necessario usare la direttiva import [**MIDL**](import.md) anziché la direttiva **\# include.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Importazione**](import.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**Includono**](include.md)
</dt> <dt>

[Importazione di file di intestazione di sistema](importing-system-header-files.md)
</dt> </dl>

 

 




