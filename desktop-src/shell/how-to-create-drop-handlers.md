---
description: Come implementare e registrare un gestore di rilascio.
title: Come creare gestori di rilascio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34c06aa3eae1892b5b86ce3a0f3b1198be41cd2f9dda5c9bd0956b40a53146e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223585"
---
# <a name="how-to-create-drop-handlers"></a>Come creare gestori di rilascio

Per impostazione predefinita, i file non sono destinazioni di rilascio. È possibile impostare i membri di un [tipo di file](fa-file-types.md) in destinazioni di rilascio implementando e registrando un gestore di *rilascio*.

Se un gestore di rilascio è registrato per un tipo di file, viene chiamato ogni volta che un oggetto viene trascinato o rilasciato su un membro del tipo di file. Shell gestisce l'operazione chiamando i metodi appropriati [**sull'interfaccia IDropTarget del**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) gestore.

Le procedure generali per l'implementazione e la registrazione di un gestore di estensioni shell sono descritte in [Creazione di gestori di estensioni della shell](handlers.md). Questo documento è in particolare sugli aspetti dell'implementazione specifici dei gestori di rilascio.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-implementing-drop-handlers"></a>Passaggio 1: Implementazione di gestori di eliminazione

Come tutti i gestori dell'estensione shell, i gestori di rilascio sono oggetti COM (In-Process Component Object Model) implementati come DLL. Esportano due interfacce oltre a [**IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

Shell inizializza il gestore tramite [**l'interfaccia IPersistFile.**](/windows/win32/api/objidl/nn-objidl-ipersistfile) Usa questa interfaccia per richiedere l'identificatore di classe (CLSID) del gestore e fornisce il nome del file. Per una descrizione generale di come implementare i gestori di estensioni shell, inclusa **l'interfaccia IPersistFile,** vedere Creazione di gestori [di estensioni della shell](handlers.md).

Dopo l'inizializzazione del gestore di rilascio, Shell chiama il metodo appropriato [**sull'interfaccia IDropTarget del**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) gestore.

### <a name="step-2-registering-drop-handlers"></a>Passaggio 2: Registrazione dei gestori di rilascio

I gestori di eliminazione vengono registrati nella sottochiave di questo tipo di file.

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

Creare una sottochiave **di DropHandler** denominata per il gestore e impostare il valore predefinito della sottochiave sul formato stringa del GUID CLSID del gestore. Per una descrizione generale di come registrare i gestori di estensioni della shell, vedere [Creazione di gestori di estensioni della shell](handlers.md).

L'esempio seguente illustra le voci del Registro di sistema che abilitano un gestore di eliminazione per un tipo di file con estensione myp di esempio.

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

[**Idroptarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[**Ipersistfile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
