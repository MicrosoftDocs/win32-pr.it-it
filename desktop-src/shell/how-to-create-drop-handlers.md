---
description: Come implementare e registrare un gestore di trascinamento.
title: Come creare i gestori di rilascio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b4349ba36a12670458a453b0622475d59d755
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227438"
---
# <a name="how-to-create-drop-handlers"></a>Come creare i gestori di rilascio

Per impostazione predefinita, i file non sono destinazioni di rilascio. È possibile rendere i membri di un [tipo di file](fa-file-types.md) in drop targets implementando e registrando un *gestore di trascinamento*.

Se un gestore di trascinamento è registrato per un tipo di file, viene chiamato ogni volta che un oggetto viene trascinato o rilasciato in un membro del tipo di file. La shell gestisce l'operazione chiamando i metodi appropriati sull'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del gestore.

Le procedure generali per l'implementazione e la registrazione di un gestore di estensione della shell sono descritte in [creazione di gestori di estensioni della shell](handlers.md). Questo documento è incentrato sugli aspetti dell'implementazione specifici dei gestori di rilascio.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-implementing-drop-handlers"></a>Passaggio 1: implementazione di gestori di rilascio

Come tutti i gestori di estensioni della shell, i gestori di rilascio sono oggetti COM (Component Object Model in-process) implementati come dll. Esportano due interfacce, oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

La shell Inizializza il gestore tramite la relativa interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Usa questa interfaccia per richiedere l'identificatore di classe del gestore (CLSID) e fornisce il nome del file. Per informazioni generali su come implementare i gestori di estensioni della shell, inclusa l'interfaccia **IPersistFile** , vedere [creazione di gestori di estensioni della shell](handlers.md).

Una volta inizializzato il gestore di trascinamento, la shell chiama il metodo appropriato sull'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del gestore.

### <a name="step-2-registering-drop-handlers"></a>Passaggio 2: registrazione di gestori di rilascio

I gestori di rilascio sono registrati nella sottochiave di questo tipo di file.

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

Creare una sottochiave di **DropHandler** denominata per il gestore, quindi impostare il valore predefinito della sottochiave sul formato stringa del GUID CLSID del gestore. Per informazioni generali su come registrare i gestori di estensioni della shell, vedere [creazione di gestori di estensioni della shell](handlers.md).

Nell'esempio seguente vengono illustrate le voci del registro di sistema che consentono un gestore di rilascio per un tipo di file example. MYP.

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
      shellex
         DropHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di gestori di estensione della shell](handlers.md)
</dt> <dt>

[**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
