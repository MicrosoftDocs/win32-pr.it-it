---
description: Il codice del prodotto è un GUID che rappresenta l'identificazione principale di un'applicazione o di un prodotto. Vedere codici prodotto.
ms.assetid: 4de84885-587d-405f-ba85-d62e09e8ba92
title: Modifica del codice del prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0272f1901ef60342f01f4db091e7a4e62b28e30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049908"
---
# <a name="changing-the-product-code"></a>Modifica del codice del prodotto

Il codice del prodotto è un GUID che rappresenta l'identificazione principale di un'applicazione o di un prodotto. Vedere [codici prodotto](product-codes.md).

Un aggiornamento che soddisfi le linee guida seguenti in genere non richiede una modifica del codice prodotto e può essere gestito come un [piccolo aggiornamento](small-updates.md)oppure, se la versione deve essere modificata, come un [aggiornamento secondario](minor-upgrades.md):

-   L'aggiornamento può ingrandire o ridurre l'albero del componente della funzionalità, ma non deve riorganizzare la gerarchia esistente di funzionalità e componenti descritti dalle tabelle [feature](feature-table.md) e [FeatureComponents](featurecomponents-table.md) . Consente di aggiungere una nuova funzionalità all'albero del componente della funzionalità esistente. Se viene rimossa una funzionalità padre, è necessario rimuovere anche tutte le funzionalità figlio della funzionalità rimossa.
-   L'aggiornamento può aggiungere un nuovo componente a una funzionalità nuova o esistente.
-   L'aggiornamento non deve modificare il codice componente di alcun componente. Di conseguenza, un aggiornamento di piccole dimensioni o un aggiornamento secondario non deve mai modificare il nome del file di chiave di un componente, perché ciò richiederebbe la modifica del codice componente.
-   L'aggiornamento non deve modificare il nome del file con estensione msi del pacchetto di installazione. Al contrario, poiché modifica il pacchetto, è necessario modificare il codice del pacchetto. Si noti che questo significa che l'aggiornamento può modificare le tabelle, le azioni personalizzate e le finestre di dialogo nel file con estensione msi senza modificare il nome del file.
-   L'aggiornamento può aggiungere, rimuovere o modificare i file, le chiavi del registro di sistema o i collegamenti di componenti che non sono condivisi da due o più funzionalità. Se l'aggiornamento modifica un file con versione, la versione del file deve essere incrementata nella [tabella file](file-table.md). Se l'aggiornamento rimuove le risorse, è necessario aggiornare anche le tabelle [RemoveFile](removefile-table.md) e [RemoveRegistry](removeregistry-table.md) per rimuovere i file non usati, le chiavi del registro di sistema o i collegamenti che sono già stati installati.
-   L'aggiornamento di un componente condiviso da due o più funzionalità deve essere compatibile con le versioni precedenti di tutte le applicazioni e le funzionalità che utilizzano il componente. L'aggiornamento può modificare la risorsa di un componente condiviso, ad esempio file, voci del registro di sistema e tasti di scelta rapida, purché le modifiche siano compatibili con le versioni precedenti. Non è consigliabile che l'aggiornamento aggiunga o Rimuovi file, voci del registro di sistema o collegamenti da un componente condiviso.
-   Un piccolo aggiornamento viene fornito come pacchetto di [patch](patch-packages.md)Windows Installer. (Un CD-ROM completo del prodotto non viene in genere fornito con un piccolo aggiornamento).

Il codice prodotto deve essere modificato se si verifica una delle condizioni seguenti per l'aggiornamento:

-   Le installazioni coesistenti di prodotti originali e aggiornati nello stesso sistema devono essere possibili.
-   Il nome del file con estensione msi è stato modificato.
-   Il codice componente di un componente esistente è stato modificato.
-   Un componente viene rimosso da una funzionalità esistente.
-   Una funzionalità esistente è stata creata in un figlio di una funzionalità esistente.
-   Una funzionalità figlio esistente è stata rimossa dalla relativa funzionalità padre.

Si noti che l'aggiunta di una nuova funzionalità figlio, costituita interamente da nuovi componenti, a una funzionalità esistente non richiede la modifica del codice del prodotto.

È possibile creare nuove funzionalità figlio includendo msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent nel campo Attributes della [tabella Feature](feature-table.md). Se l'aggiornamento secondario aggiunge solo nuove funzionalità figlio, reinstallare = ALL è sufficiente per forzare l'installazione delle nuove funzionalità figlio. Per ulteriori informazioni, vedere [controllo degli Stati di selezione delle funzionalità](controlling-feature-selection-states.md).

Una nuova funzionalità figlio potrebbe essere nascosta all'utente. Per sincronizzare lo stato di installazione di una nuova funzionalità figlio con la relativa funzionalità padre, impostare i bit msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent per la funzionalità figlio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle proprietà](about-properties.md)
</dt> <dt>

[Utilizzo delle proprietà](using-properties.md)
</dt> <dt>

[Riferimento alla proprietà](property-reference.md)
</dt> </dl>

 

 



