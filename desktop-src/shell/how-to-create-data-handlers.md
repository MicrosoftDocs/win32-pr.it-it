---
description: Estensione degli Appunti con gestori del formato dati personalizzati.
title: Come creare i gestori di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ecc08769068d975c1fa16ef1385f362c67e43c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994685"
---
# <a name="how-to-create-data-handlers"></a>Come creare i gestori di dati

Quando un file viene copiato negli Appunti o trascinato e rilasciato, la shell crea un oggetto dati che supporta una varietà di [formati degli Appunti](dragdrop.md)standard. Per i file di un tipo di file specifico, è possibile estendere i formati degli appunti disponibili implementando e registrando un *gestore di dati*. Quando viene trasferito un file del tipo di file, la shell delega le chiamate all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati al gestore dati se viene utilizzato uno dei formati personalizzati.

Le procedure generali per l'implementazione e la registrazione di un gestore di estensione della shell sono descritte in [creazione di gestori di estensioni della shell](handlers.md). Questo documento è incentrato sugli aspetti dell'implementazione specifici dei gestori di dati.

-   [Implementazione di gestori di dati](#step-1-implementing-data-handlers)
-   [Registrazione dei gestori di dati](#step-2-registering-data-handlers)
-   [Argomenti correlati](#related-topics)

## <a name="instructions"></a>Istruzioni

### <a name="step-1-implementing-data-handlers"></a>Passaggio 1: implementazione di gestori di dati

Come tutti i gestori di estensioni della shell, i gestori di dati sono oggetti Component Object Model in-process (COM) implementati come dll. Esportano due interfacce, oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).

La shell Inizializza il gestore tramite la relativa interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Usa questa interfaccia per richiedere l'identificatore di classe del gestore (CLSID) e fornisce il nome del file. Per informazioni generali su come implementare i gestori di estensioni della shell, inclusa l'interfaccia **IPersistFile** , vedere [creazione di gestori di estensioni della shell](handlers.md).

Una volta inizializzato il gestore dati, la shell delega le chiamate dall'oggetto dati all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del gestore se viene utilizzato uno dei formati personalizzati.

### <a name="step-2-registering-data-handlers"></a>Passaggio 2: registrazione dei gestori di dati

I gestori di dati sono registrati nella sottochiave *ProgID* del tipo di file, come illustrato di seguito: **HKEY \_ classi \_ radice** \\ *ProgID* \\ **ShellEx** \\ **DataHandler**

Creare una sottochiave denominata per il gestore in **DataHandler** e impostare il valore predefinito della sottochiave di tale gestore sul formato stringa del GUID CLSID del gestore. Per informazioni generali su come registrare i gestori di estensioni della shell, vedere [creazione di gestori di estensioni della shell](handlers.md).

Nell'esempio seguente vengono illustrate le voci del registro di sistema che consentono un gestore di dati per un tipo di file con estensione MYP.

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

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
