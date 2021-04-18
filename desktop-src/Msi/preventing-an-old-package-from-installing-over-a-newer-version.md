---
description: Se per un utente è già installata una versione più recente, è possibile creare pacchetti di aggiornamento Windows Installer per eseguire aggiornamenti principali.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Impedisci l'installazione di un pacchetto obsoleto in una versione più recente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320ab062c4ffbc740d85c59ece3d3baaa63f4209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310968"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a>Impedire l'installazione di un pacchetto obsoleto in una versione più recente

Se per un utente è già installata una versione più recente, è possibile creare pacchetti di aggiornamento Windows Installer per eseguire aggiornamenti principali. La procedura descritta in questo argomento può impedire solo i downgrade che potrebbero essere causati dall'esecuzione di un pacchetto di aggiornamento principale. Questa procedura si basa sull' [azione FindRelatedProducts](findrelatedproducts-action.md), che viene eseguita solo durante un'installazione per la prima volta e non viene eseguita in modalità di manutenzione (reinstallazione). Poiché gli aggiornamenti secondari vengono eseguiti con la reinstallazione, questa procedura non può essere utilizzata per determinare se un pacchetto di aggiornamento secondario tenta di effettuare il downgrade di un'applicazione. Per ulteriori informazioni, vedere [preparazione di un'applicazione per aggiornamenti principali futuri](preparing-an-application-for-future-major-upgrades.md).

**Per impedire l'installazione di un pacchetto obsoleto in una versione più recente**

1.  Immettere la proprietà [**UpgradeCode**](upgradecode.md) per il gruppo di prodotti correlati che potrebbero essere idonei a ricevere questo aggiornamento nella colonna UpgradeCode della [tabella di aggiornamento](upgrade-table.md).
2.  Immettere il flag di bit **msidbUpgradeAttributesOnlyDetect** nella colonna attributi della [tabella di aggiornamento](upgrade-table.md).
3.  Immettere la versione dell'aggiornamento fornito dal pacchetto nella colonna VersionMin della [tabella di aggiornamento](upgrade-table.md). Lasciare vuota la colonna VersionMax.
4.  Immettere il nome della proprietà che deve essere impostata dall' [azione FindRelatedProducts](findrelatedproducts-action.md) nella colonna ActionProperty della [tabella di aggiornamento](upgrade-table.md).
5.  Aggiungere la proprietà [**SecureCustomProperties**](securecustomproperties.md) e la proprietà denominata nella colonna ActionProperty della tabella di [aggiornamento](upgrade-table.md) alla tabella delle [proprietà](property-table.md).
6.  Aggiungere un [tipo di azione personalizzata 19](custom-action-type-19.md) dopo l'azione FindRelatedProducts nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Includere un record nella [tabella CustomAction](customaction-table.md) per questa azione e immettere il testo da visualizzare nella colonna destinazione. Il tipo 19 azione personalizzata è incorporato nel programma di installazione, quindi non è disponibile codice da scrivere.
7.  Immettere il nome del ActionProperty nella colonna condizione del record nella [tabella InstallExecuteSequence](installexecutesequence-table.md) che contiene il [tipo di azione personalizzata 19](custom-action-type-19.md). Questa condizione consente di eseguire l'azione personalizzata solo quando la [tabella di aggiornamento](upgrade-table.md) rileva che è già installata una versione più recente.

    Ad esempio, un pacchetto di Windows Installer che aggiorna un gruppo di prodotti correlati alla versione 3,0 può includere i record seguenti nelle tabelle di [aggiornamento](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md)e [Proprietà](property-table.md) . Tutti i prodotti correlati del gruppo hanno lo stesso UpgradeCode, ma il programma di installazione non installa il pacchetto di aggiornamento se una versione successiva alla 3,0 è già installata nel computer. In questo caso, il programma di installazione visualizza un messaggio di errore e l'installazione ha esito negativo. Il pacchetto di aggiornamento versione 3,0 viene installato nelle versioni 1,0 e 2,0.

    [Aggiorna tabella](upgrade-table.md)

    

    | UpgradeCode                            | VersionMin | VersionMax | Linguaggio | Attributi                                | Rimuovi | ActionProperty  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 3.0        |            |          | msidbUpgradeAttributesOnlyDetect          |        | NEWPRODUCTFOUND |
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 1.0        | 3.0        |          | msidbUpgradeAttributesVersionMinInclusive |        | UPGRADEFOUND    |

    

     

    [Tabella CustomAction](customaction-table.md)

    

    | Azione | Tipo | Source (Sorgente) | Destinazione                                 |
    |--------|------|--------|----------------------------------------|
    | CA1    | 19   |        | È già installato un aggiornamento superiore. |

    

     

    [Tabella InstallExecuteSequence](installexecutesequence-table.md)

    

    | Azione              | Condizione       | Sequenza |
    |---------------------|-----------------|----------|
    | FindRelatedProducts |                 | 200      |
    | CA1                 | NEWPRODUCTFOUND | 201      |

    

     

    [Tabella delle proprietà](property-table.md)

    

    | Proprietà                                                 | Valore                        |
    |----------------------------------------------------------|------------------------------|
    | [**SecureCustomProperties**](securecustomproperties.md) | NEWPRODUCTFOUND; UPGRADEFOUND |

    

     

 

 



