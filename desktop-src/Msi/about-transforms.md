---
description: Una trasformazione è una raccolta di modifiche applicate a un'installazione. Applicando una trasformazione a un pacchetto di installazione di base, il programma di installazione può aggiungere o sostituire i dati nel database di installazione. Il programma di installazione può applicare le trasformazioni solo durante un'installazione.
ms.assetid: 1edc5227-70ac-4769-ab7f-67d01031dc33
title: Informazioni sulle trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbae9f21ec71209116f3c8eadffca20381cfe71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227225"
---
# <a name="about-transforms"></a>Informazioni sulle trasformazioni

Una trasformazione è una raccolta di modifiche applicate a un'installazione. Applicando una trasformazione a un pacchetto di installazione di base, il programma di installazione può aggiungere o sostituire i dati nel database di installazione. Il programma di installazione può applicare le trasformazioni solo durante un'installazione.

Il programma di installazione registra un elenco di trasformazioni richieste dal prodotto durante l'installazione. Il programma di installazione deve applicare tali trasformazioni al pacchetto di installazione del prodotto durante la configurazione o l'installazione del prodotto. Se una trasformazione elencata non è disponibile e se la resilienza dell'origine della trasformazione non è in grado di ripristinarla, l'installazione non riesce.

Una trasformazione può modificare le informazioni presenti in qualsiasi tabella persistente nel [database del programma di installazione](installer-database.md). Una trasformazione consente inoltre di aggiungere o rimuovere tabelle permanenti nel database del programma di installazione. Le trasformazioni non possono modificare alcuna parte di un pacchetto di installazione che non si trova in una tabella di database, ad esempio le informazioni nel [flusso di informazioni di riepilogo](summary-information-stream.md), le informazioni contenute nelle sottoarchiviazioni o i file in file CAB incorporati.

Le trasformazioni includono un flusso di informazioni di riepilogo che può contenere condizioni di convalida e condizioni di errore. La convalida della trasformazione e le condizioni di errore possono essere aggiunte alle informazioni di riepilogo tramite la funzione [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) . Le condizioni di convalida controllano se il programma di installazione può applicare la trasformazione a un determinato database di installazione. La convalida della trasformazione può essere condizionata in base ai valori delle proprietà [**UpgradeCode**](upgradecode.md), [**ProductCode**](productcode.md), [**ProductVersion**](productversion.md) e [**ProductLanguage**](productlanguage.md) specificate nella trasformazione e a quelle del database di installazione. Le condizioni di errore di trasformazione controllano gli errori che vengono eliminati quando si applica la trasformazione. Le condizioni di errore incluse nella trasformazione vengono sottoposte a override dalle condizioni di errore specificate usando i metodi [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) e [**ApplyTransform**](database-applytransform.md) .

> [!Note]  
> Le trasformazioni di personalizzazione tipiche non hanno condizioni di convalida né convalidate in base a [**ProductCode**](productcode.md). Le trasformazioni archiviate nei [pacchetti di patch](patch-packages.md) hanno in genere rigide condizioni di convalida per garantire che la trasformazione corretta venga applicata alla destinazione della patch.

 

Sono disponibili tre tipi di trasformazioni Windows Installer:

-   [Trasformazioni incorporate](embedded-transforms.md)
-   [Trasformazioni protette](secured-transforms.md)
-   [Trasformazioni non protette](unsecured-transforms.md)

 

 



