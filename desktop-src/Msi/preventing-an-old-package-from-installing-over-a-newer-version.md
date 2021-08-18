---
description: Windows I pacchetti di aggiornamento del programma di installazione possono essere creati in modo che gli aggiornamenti principali non siano installati se per un utente è già installata una versione più recente.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Impedire l'installazione di un pacchetto precedente in una versione più recente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e992cc1e32d2b25e5af587c00ca4f8ee28e4b09fd3100cb12b382ae90f8c1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145384"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a>Impedire l'installazione di un pacchetto precedente in una versione più recente

Windows I pacchetti di aggiornamento del programma di installazione possono essere creati in modo che gli aggiornamenti principali non siano installati se per un utente è già installata una versione più recente. La procedura descritta in questo argomento può impedire solo i downgrade che potrebbero essere causati dall'esecuzione di un pacchetto di aggiornamento principale. Questa procedura si basa sull'azione [FindRelatedProducts](findrelatedproducts-action.md), che viene eseguita solo durante una prima installazione e non in modalità di manutenzione (reinstallazione). Poiché gli aggiornamenti secondari vengono eseguiti tramite reinstallazione, questa procedura non può essere utilizzata per determinare se un pacchetto di aggiornamento secondario sta tentando di effettuare il downgrade di un'applicazione. Per altre informazioni, vedere [Preparazione di un'applicazione per gli aggiornamenti principali futuri.](preparing-an-application-for-future-major-upgrades.md)

**Per impedire l'installazione di un pacchetto precedente in una versione più recente**

1.  Immettere la [**proprietà UpgradeCode**](upgradecode.md) per il gruppo di prodotti correlati che possono essere idonei per ricevere l'aggiornamento nella colonna UpgradeCode della [tabella di aggiornamento](upgrade-table.md).
2.  Immettere il flag di bit **msidbUpgradeAttributesOnlyDetect** nella colonna Attributi della [tabella di aggiornamento](upgrade-table.md).
3.  Immettere la versione dell'aggiornamento fornito da questo pacchetto nella colonna VersionMin della [tabella di aggiornamento](upgrade-table.md). Lasciare vuota la colonna VersionMax.
4.  Immettere il nome della proprietà che deve essere impostata dall'azione [FindRelatedProducts](findrelatedproducts-action.md) nella colonna ActionProperty di [Upgrade Table](upgrade-table.md).
5.  Aggiungere la [**proprietà SecureCustomProperties**](securecustomproperties.md) e la proprietà denominata nella colonna ActionProperty di [Upgrade Table](upgrade-table.md) alla tabella [delle proprietà](property-table.md).
6.  Aggiungere [un'azione personalizzata di tipo 19](custom-action-type-19.md) dopo l'azione FindRelatedProducts nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Includere un record nella [tabella CustomAction per](customaction-table.md) questa azione e immettere il testo da visualizzare nella colonna Destinazione. L'azione personalizzata di tipo 19 è incorporata nel programma di installazione, quindi non è disponibile codice da scrivere.
7.  Immettere il nome di ActionProperty nella colonna Condizione del record nella tabella [InstallExecuteSequence](installexecutesequence-table.md) che contiene il [tipo di azione personalizzata 19.](custom-action-type-19.md) In questo modo l'azione personalizzata [](upgrade-table.md) viene eseguita solo quando la tabella di aggiornamento rileva che è già installata una versione più recente.

    Ad esempio, un pacchetto del programma di installazione di Windows che aggiorna un gruppo di prodotti correlati alla versione 3.0 può includere i record seguenti nelle tabelle [Upgrade](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md)e [Property.](property-table.md) Tutti i prodotti correlati nel gruppo hanno lo stesso UpgradeCode, ma il programma di installazione non installa questo pacchetto di aggiornamento se nel computer è già installata una versione successiva alla 3.0. In questo caso, il programma di installazione visualizza un messaggio di errore e l'installazione non riesce. Il pacchetto di aggiornamento della versione 3.0 viene installato nelle versioni 1.0 e 2.0.

    [Aggiorna tabella](upgrade-table.md)

    

    | Codice di aggiornamento                            | VersionMin | VersionMax | Linguaggio | Attributi                                | Rimuovi | ActionProperty  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 3.0        |            |          | msidbUpgradeAttributesOnlyDetect          |        | NEWPRODUCTFOUND |
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 1.0        | 3.0        |          | msidbUpgradeAttributesVersionMinInclusive |        | UPGRADEFOUND    |

    

     

    [Tabella CustomAction](customaction-table.md)

    

    | Azione | Tipo | Source (Sorgente) | Destinazione                                 |
    |--------|------|--------|----------------------------------------|
    | CA1    | 19   |        | È già installato un aggiornamento superiore. |

    

     

    [Tabella InstallExecuteSequence](installexecutesequence-table.md)

    

    | Azione              | Condition       | Sequenza |
    |---------------------|-----------------|----------|
    | FindRelatedProducts |                 | 200      |
    | CA1                 | NEWPRODUCTFOUND | 201      |

    

     

    [Tabella delle proprietà](property-table.md)

    

    | Proprietà                                                 | Valore                        |
    |----------------------------------------------------------|------------------------------|
    | [**SecureCustomProperties**](securecustomproperties.md) | NEWPRODUCTFOUND; UPGRADEFOUND |

    

     

 

 



