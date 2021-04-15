---
title: Classi e associazioni predefinite
description: Per alcune categorie, una singola classe può essere associata come classe predefinita.
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871c537535c57da0809effbe3ee8ec086a88fd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395327"
---
# <a name="default-classes-and-associations"></a>Classi e associazioni predefinite

Per alcune categorie, una singola classe può essere associata come classe predefinita. La classe predefinita viene selezionata ogni volta che è richiesta una particolare categoria di oggetti. Sebbene questo potrebbe non essere utile per tutte le categorie di componenti, la definizione di una classe predefinita può essere utile quando è necessario caricare una determinata classe da un elenco di classi possibili senza l'intervento dell'utente. Gli amministratori definiscono la classe che può essere utilizzata modificando il registro di sistema.

Per associare una classe predefinita a una categoria, introdurre una chiave CLSID con lo stesso CLSID del CATId della categoria del componente scelto come valore predefinito. Quindi aggiungere una chiave Treats a questa chiave, usando il valore per il CLSID della classe predefinita per la categoria. Per usare la classe predefinita per una categoria di componenti, usare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), specificando il CATID per il parametro CLSID. Viene automaticamente reindirizzato al CLSID definito come valore predefinito per questa categoria. La voce del registro di sistema è la seguente:

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

Durante l'installazione, un componente può verificare l'esistenza di eventuali chiavi di classe predefinite per le relative categorie e presentare all'utente le opzioni per l'override delle impostazioni correnti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione di icone a una categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizzazione in base alle funzionalità del componente](categorizing-by-component-capabilities.md)
</dt> <dt>

[Categorizzazione in base alle funzionalità del contenitore](categorizing-by-container-capabilities.md)
</dt> <dt>

[Definizione delle categorie di componenti](defining-component-categories.md)
</dt> <dt>

[Gestione categorie di componenti](the-component-categories-manager.md)
</dt> </dl>

 

 




