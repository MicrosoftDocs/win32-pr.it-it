---
description: Viene descritto come creare un gestore per le assegnazioni di icone personalizzate.
ms.assetid: 23ed3a21-cf62-4440-b983-fae23aa56890
title: Come creare gestori di icone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c620b6f6a4c05f8996a26c8365e4f4201ee0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979599"
---
# <a name="how-to-create-icon-handlers"></a>Come creare gestori di icone

A un [tipo di file](fa-file-types.md) è spesso associata un'icona personalizzata, per rendere i membri facilmente riconoscibili in Esplora risorse. Il modo più semplice per assegnare un'icona personalizzata a un tipo di file consiste nel registrare il file dell'icona. Tuttavia, un'icona registrata in questo modo sarà la stessa per tutti i membri del tipo di file. È possibile disporre di una maggiore flessibilità nell'assegnazione delle icone ai membri del tipo di file mediante l'implementazione di un *gestore di icone*.

Un gestore di icone è un tipo di gestore di estensione della shell che consente di assegnare dinamicamente icone ai membri di un tipo di file. Ogni volta che viene visualizzato un file di tipo, la shell esegue una query sul gestore per l'icona appropriata. Ad esempio, un gestore di icone può assegnare icone diverse a membri diversi del tipo di file o variare l'icona in base allo stato corrente del file.

Le procedure generali per l'implementazione e la registrazione di un gestore di estensione della shell sono descritte in [creazione di gestori di estensioni della shell](handlers.md). Questo documento è incentrato sugli aspetti dell'implementazione specifici dei gestori di icone.

-   [Implementazione di gestori di icone](#step-1-implementing-icon-handlers)
-   [Implementazione dell'interfaccia IExtractIcon](#step-2-implementing-the-iextracticon-interface)
-   [Registrazione di gestori di icone](#step-3-registering-icon-handlers)
-   [Argomenti correlati](#related-topics)

## <a name="instructions"></a>Istruzioni

### <a name="step-1-implementing-icon-handlers"></a>Passaggio 1: implementazione di gestori di icone

Come tutti i gestori di estensioni della shell, i gestori di icone sono oggetti COM (Component Object Model in-process) implementati come dll. Devono esportare due interfacce, oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) e [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).

La shell Inizializza il gestore tramite la relativa interfaccia [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Usa questa interfaccia per richiedere l'identificatore di classe del gestore (CLSID) e fornisce il nome del file. Il resto dell'operazione viene eseguita tramite l'interfaccia [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) . Per informazioni generali su come implementare i gestori di estensioni della shell, inclusa l'interfaccia **IPersistFile** , vedere [creazione di gestori di estensioni della shell](handlers.md). Nella parte restante di questo documento viene illustrato come implementare l'interfaccia **IExtractIcon** .

### <a name="step-2-implementing-the-iextracticon-interface"></a>Passaggio 2: implementazione dell'interfaccia IExtractIcon

Dopo l'inizializzazione dell'interfaccia, la shell usa l'interfaccia [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) del gestore per richiedere l'icona appropriata. L'interfaccia dispone di due metodi: [**IExtractIcon:: GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) e [**IExtractIcon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract).

Le icone vengono identificate in base alla relativa posizione nella file system. Per richiedere queste informazioni, viene chiamato il metodo [**IExtractIcon:: GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) . Impostare il parametro *szIconFile* sul nome del file. Se nel file è presente più di un'icona, impostare *piIndex* sull'indice dell'icona. Assegnare i valori appropriati alle due variabili del flag. Se non si vuole specificare un nome di file o se non si vuole che la shell estragga l'icona, impostare il flag **Gil \_ NOTFILENAME** nel parametro *pwFlags* . Non è necessario assegnare un valore a *szIconFile*, ma il gestore deve fornire handle di icona quando la shell chiama [**IExtractIcon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract).

Se si restituisce un nome di file, la shell tenta in genere di caricare l'icona dalla relativa cache. Per evitare il caricamento di un'icona memorizzata nella cache, impostare il flag **Gil \_ DONTCACHE** nel parametro *pwFlags* . Se non viene caricata un'icona memorizzata nella cache, la shell chiama [**IExtractIcon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) per richiedere l'handle dell'icona.

Se un file e un indice sono stati specificati da [**IExtractIcon:: GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation), vengono passati rispettivamente a [**IExtractIcon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) nei parametri *pszFile* e *nIconIndex* . Se viene fornito un nome di file, il gestore può restituire S \_ false per fare in modo che la shell estragga l'icona. In caso contrario, il gestore deve estrarre o produrre icone grandi e piccole, quindi assegnare i rispettivi handle HICON ai parametri *phiconLarge* e *phiconSmall* . La shell aggiunge le icone alla relativa cache per velocizzare le chiamate successive al gestore.

### <a name="step-3-registering-icon-handlers"></a>Passaggio 3: registrazione di gestori di icone

Quando si [registra in modo statico un'icona](icon.md) per un [tipo di file](fa-file-types.md), si crea una sottochiave **DefaultIcon** in ProgID per il tipo di file. Il valore predefinito è impostato sul file che contiene l'icona. Per registrare un gestore di icone, è necessario avere ancora la sottochiave **DefaultIcon** , ma il valore predefinito deve essere impostato su "%1". Aggiungere una sottochiave **IconHandler** alla sottochiave **ShellEx** della sottochiave ProgID e impostarne il valore predefinito sul formato stringa del GUID CLSID del gestore. Per informazioni generali su come registrare i gestori di estensioni della shell, vedere [creazione di gestori di estensioni della shell](handlers.md).

Nell'esempio seguente la voce del registro di sistema viene modificata dalle [Icone di personalizzazione](icon.md) in modo che il tipo di file. MYP ora usi un gestore di menu di scelta rapida anziché un'icona definita in modo statico.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = %1
      Shellex
         IconHandler
            (Default) = {The handler's CLSID GUID}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di gestori di estensione della shell](handlers.md)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)
</dt> </dl>

 

 
