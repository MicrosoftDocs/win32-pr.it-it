---
description: Estensione degli Appunti con gestori di formati di dati personalizzati.
title: Come creare gestori dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a3761b4dc8ce3e7d50d967d2267971537d3609e7a7cf76785623734558adac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715051"
---
# <a name="how-to-create-data-handlers"></a>Come creare gestori dati

Quando un file viene copiato negli Appunti o trascinato e rilasciato, la shell crea un oggetto dati che supporta un'ampia gamma di formati di [Appunti](dragdrop.md)standard. Per i file di un tipo di file specifico, è possibile estendere i formati degli Appunti disponibili implementando e registrando un *gestore dati*. Quando viene trasferito un file del tipo di file, la shell delega le chiamate all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati al gestore dati se viene usato uno dei formati personalizzati.

Le procedure generali per l'implementazione e la registrazione di un gestore estensioni della shell sono descritte in [Creazione di gestori di estensioni della shell.](handlers.md) Questo documento è in particolare sugli aspetti dell'implementazione specifici dei gestori dati.

-   [Implementazione di gestori dati](#step-1-implementing-data-handlers)
-   [Registrazione di gestori dati](#step-2-registering-data-handlers)
-   [Argomenti correlati](#related-topics)

## <a name="instructions"></a>Istruzioni

### <a name="step-1-implementing-data-handlers"></a>Passaggio 1: Implementazione di gestori dati

Come tutti i gestori di estensioni della shell, i gestori dati sono oggetti COM (In-Process Component Object Model) implementati come DLL. Esportano due interfacce oltre a [**IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDataObject.**](/windows/win32/api/objidl/nn-objidl-idataobject)

La shell inizializza il gestore tramite la relativa [**interfaccia IPersistFile.**](/windows/win32/api/objidl/nn-objidl-ipersistfile) Usa questa interfaccia per richiedere l'identificatore di classe (CLSID) del gestore e fornisce il nome del file. Per una descrizione generale di come implementare i gestori di estensioni della shell, inclusa **l'interfaccia IPersistFile,** vedere Creazione di gestori di [estensioni della shell.](handlers.md)

Dopo l'inizializzazione del gestore dati, la shell delega le chiamate dall'oggetto dati all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del gestore se viene usato uno dei formati personalizzati.

### <a name="step-2-registering-data-handlers"></a>Passaggio 2: Registrazione dei gestori dati

I gestori di dati vengono registrati nella sottochiave *ProgID* del tipo di file, come illustrato di seguito: **HKEY \_ CLASSES \_ ROOT** \\ *ProgID* \\ **shellex** \\ **DataHandler**

Creare una sottochiave denominata per il gestore in **DataHandler** e impostare il valore predefinito della sottochiave del gestore sul formato stringa del GUID CLSID del gestore. Per una descrizione generale di come registrare i gestori di estensioni della shell, vedere [Creazione di gestori di estensioni della shell.](handlers.md)

Nell'esempio seguente vengono illustrate le voci del Registro di sistema che abilitano un gestore dati per un tipo di file myp di esempio.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         DataHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di gestori di estensione della shell](handlers.md)
</dt> <dt>

[**Ipersistfile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**Idataobject**](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
