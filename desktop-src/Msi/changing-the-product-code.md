---
description: Il codice prodotto è un GUID che rappresenta l'identificazione principale di un'applicazione o di un prodotto. Vedere Codici prodotto.
ms.assetid: 4de84885-587d-405f-ba85-d62e09e8ba92
title: Modifica del codice prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4567cbb014fa2f2002f0433a8e42c3a261ccb1af350f9b4e592a3bb5ff8a0216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340011"
---
# <a name="changing-the-product-code"></a>Modifica del codice prodotto

Il codice prodotto è un GUID che rappresenta l'identificazione principale di un'applicazione o di un prodotto. Vedere [Codici prodotto](product-codes.md).

Un aggiornamento che soddisfa le linee guida seguenti in genere non richiede una modifica del codice del prodotto e può essere gestito come un piccolo aggiornamento [o,](small-updates.md)se la versione deve cambiare, come aggiornamento [secondario:](minor-upgrades.md)

-   L'aggiornamento può ingrandire o ridurre l'albero funzionalità-componente, ma non deve riorganizzare la gerarchia esistente di funzionalità e componenti descritta dalle tabelle [Feature](feature-table.md) e [FeatureComponents.](featurecomponents-table.md) Può aggiungere una nuova funzionalità all'albero funzionalità-componente esistente. Se rimuove una funzionalità padre, deve rimuovere anche tutte le funzionalità figlio della funzionalità rimossa.
-   L'aggiornamento può aggiungere un nuovo componente a una funzionalità nuova o esistente.
-   L'aggiornamento non deve modificare il codice del componente di alcun componente. Di conseguenza, un aggiornamento di piccole dimensioni o secondario non deve mai modificare il nome del file di chiave di un componente perché ciò richiederebbe la modifica del codice del componente.
-   L'aggiornamento non deve modificare il nome del .msi del pacchetto di installazione. Al contrario, poiché modifica il pacchetto, deve modificare il codice del pacchetto. Si noti che questo significa che l'aggiornamento può modificare le tabelle, le azioni personalizzate e le finestre di dialogo nel file .msi senza modificare il nome del file.
-   L'aggiornamento può aggiungere, rimuovere o modificare i file, le chiavi del Registro di sistema o i collegamenti di componenti non condivisi da due o più funzionalità. Se l'aggiornamento modifica un file con controllo delle versioni, la versione del file deve essere incrementata nella [tabella File](file-table.md). Se l'aggiornamento rimuove le risorse, deve anche aggiornare le tabelle [RemoveFile](removefile-table.md) e [RemoveRegistry](removeregistry-table.md) per rimuovere eventuali file inutilizzati, chiavi del Registro di sistema o collegamenti già installati.
-   L'aggiornamento di un componente condiviso da due o più funzionalità deve essere compatibile con le versioni precedenti di tutte le applicazioni e le funzionalità che usano il componente. L'aggiornamento può modificare la risorsa di un componente condiviso, ad esempio file, voci del Registro di sistema e collegamenti, purché le modifiche siano compatibili con le versioni precedenti. Non è consigliabile aggiungere o rimuovere file, voci del Registro di sistema o collegamenti da un componente condiviso.
-   Un piccolo aggiornamento viene fornito come pacchetto di patch Windows installer [.](patch-packages.md) Un CD-ROM completo del prodotto non viene in genere fornito con un piccolo aggiornamento.

Il codice del prodotto deve essere modificato se una delle condizioni seguenti è vera per l'aggiornamento:

-   Devono essere possibili installazioni coesistenti di prodotti originali e aggiornati nello stesso sistema.
-   Il nome del .msi file è stato modificato.
-   Il codice del componente di un componente esistente è stato modificato.
-   Un componente viene rimosso da una funzionalità esistente.
-   Una funzionalità esistente è stata trasformata in un elemento figlio di una funzionalità esistente.
-   Una funzionalità figlio esistente è stata rimossa dalla relativa funzionalità padre.

Si noti che l'aggiunta di una nuova funzionalità figlio, costituita interamente da nuovi componenti, a una funzionalità esistente non richiede la modifica del codice del prodotto.

È possibile creare nuove funzionalità figlio includendo msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent nel campo Attributi della tabella [Funzionalità](feature-table.md). Se l'aggiornamento secondario aggiunge solo nuove funzionalità figlio, REINSTALL=ALL è sufficiente per forzare l'installazione delle nuove funzionalità figlio. Per altre informazioni, vedere [Controllo degli stati di selezione delle funzionalità](controlling-feature-selection-states.md).

Una nuova funzionalità figlio può essere nascosta all'utente. Per sincronizzare lo stato di installazione di una nuova funzionalità figlio con la relativa funzionalità padre, impostare i bit msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent per la funzionalità figlio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle proprietà](about-properties.md)
</dt> <dt>

[Utilizzo delle proprietà](using-properties.md)
</dt> <dt>

[Informazioni di riferimento sulla proprietà](property-reference.md)
</dt> </dl>

 

 



