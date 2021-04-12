---
title: Importazione di file e librerie dei tipi
description: Le parole chiave MIDL includono, import e importlib consentono di riutilizzare il codice facendo riferimento ai file di intestazione, IDL e di definizione degli oggetti (FAD) esistenti e alle librerie dei tipi compilate.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Microsoft Interface Definition Language MIDL, attività, importazione di file e librerie dei tipi
- importazione di MIDL
- librerie di tipi MIDL, importazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b740f29726c1ce4d401fc69b2ea07e811eac0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353991"
---
# <a name="importing-files-and-type-libraries"></a>Importazione di file e librerie dei tipi

Le parole chiave MIDL [**includono**](include.md), [**Import**](import.md)e [**importlib**](importlib.md) consentono di riutilizzare il codice facendo riferimento ai file di intestazione, IDL e di definizione degli oggetti (FAD) esistenti e alle librerie dei tipi compilate.

Con la direttiva ACF [**include**](include.md) è possibile specificare in un file ACF uno o più file di intestazione del linguaggio C da includere nel codice stub generato da MIDL. Il file generato avrà una riga con una direttiva **\# Includi** il preprocessore C con il file di intestazione indicato. Usare questa direttiva **include per inserire** i file di intestazione specifici di un determinato ambiente operativo e che non contengono informazioni necessarie per l'interfaccia tra client e server. Non utilizzare **Includi** per i file di intestazione che contengono i tipi di dati che si desidera siano disponibili per il file IDL. usare invece la direttiva [**Import**](import.md) .

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

La direttiva di [**importazione**](import.md) IDL è il metodo standard per portare le definizioni di tipo e interfaccia da altri file IDL (o FAD) e file di intestazione nel file IDL. Tutte le istruzioni IDL nel file importato, ad esempio i typedef, le dichiarazioni [**const**](const.md) e le definizioni di interfaccia, diventano disponibili per il file IDL di importazione.

Analogamente alla direttiva per il preprocessore del linguaggio **C, la direttiva \#** [**Import**](import.md) indica al compilatore di includere i tipi di dati definiti nei file IDL importati. A differenza della direttiva **\# include** , la direttiva **Import** ignora i prototipi di routine, perché non vengono generati stub per alcun elemento nel file importato. Poiché il preprocessore viene richiamato separatamente per il file importato, le direttive per il preprocessore, ad esempio * *, non vengono riportate nel file IDL di importazione.

Per ulteriori informazioni sull'utilizzo dell' [**importazione**](import.md) per includere i file di intestazione di sistema in un file IDL, vedere [importazione di file di intestazione di sistema](importing-system-header-files.md).

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

La direttiva [**importlib**](importlib.md) di FAD consente di fare riferimento a una libreria dei tipi compilata nel file IDL o FAD. La direttiva **importlib** deve trovarsi all'interno di un'istruzione [**Library**](library.md) e deve precedere altre descrizioni dei tipi nella libreria. La libreria importata, così come la libreria generata, deve essere disponibile per l'applicazione in fase di esecuzione.

## <a name="example-3"></a>Esempio 3

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

È anche possibile usare la direttiva di **\# inclusione** del preprocessore C per includere intestazioni e altri file nel file IDL o FAD. Tenere presente, tuttavia, che questa direttiva includerà letteralmente l'intero contenuto del file specificato. Se un file di intestazione contiene prototipi non necessari o desiderati nei file stub generati da MIDL o se contiene definizioni di tipi non, è necessario usare la direttiva di [**importazione**](import.md) MIDL invece della direttiva **\# include** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**importare**](import.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**includere**](include.md)
</dt> <dt>

[Importazione di file di intestazione di sistema](importing-system-header-files.md)
</dt> </dl>

 

 




