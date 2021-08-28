---
description: Una trasformazione è una raccolta di modifiche applicate a un'installazione. Applicando una trasformazione a un pacchetto di installazione di base, il programma di installazione può aggiungere o sostituire dati nel database di installazione. Il programma di installazione può applicare trasformazioni solo durante un'installazione.
ms.assetid: 1edc5227-70ac-4769-ab7f-67d01031dc33
title: Informazioni sulle trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 635430fb5e75b658880d5c5670219cae950502421c2b188af0381fd60ad3d48e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013269"
---
# <a name="about-transforms"></a>Informazioni sulle trasformazioni

Una trasformazione è una raccolta di modifiche applicate a un'installazione. Applicando una trasformazione a un pacchetto di installazione di base, il programma di installazione può aggiungere o sostituire dati nel database di installazione. Il programma di installazione può applicare trasformazioni solo durante un'installazione.

Il programma di installazione registra un elenco di trasformazioni richieste dal prodotto durante l'installazione. Il programma di installazione deve applicare queste trasformazioni al pacchetto di installazione del prodotto durante la configurazione o l'installazione del prodotto. Se una trasformazione elencata non è disponibile e la resilienza dell'origine della trasformazione non è in grado di ripristinarla, l'installazione non riesce.

Una trasformazione può modificare le informazioni contenute in qualsiasi tabella persistente nel [database del programma di installazione](installer-database.md). Una trasformazione può anche aggiungere o rimuovere tabelle persistenti nel database del programma di installazione. Le trasformazioni non possono modificare parti di un pacchetto di installazione che non si trova in una tabella di database, ad esempio informazioni nel flusso di informazioni di [riepilogo,](summary-information-stream.md)informazioni in archivi secondari o file in archivi incorporati.

Le trasformazioni hanno un flusso di informazioni di riepilogo che può contenere condizioni di convalida e condizioni di errore. La convalida della trasformazione e le condizioni di errore possono essere aggiunte alle informazioni di riepilogo usando la [**funzione MsiCreateTransformSummaryInfo.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) Le condizioni di convalida controllano se il programma di installazione può applicare la trasformazione a un database di installazione specificato. La convalida della trasformazione può essere condizionata in base ai valori delle proprietà [**UpgradeCode**](upgradecode.md), [**ProductCode**](productcode.md), [**ProductVersion**](productversion.md) [**e ProductLanguage**](productlanguage.md) specificate nella trasformazione e a quelli del database di installazione. Le condizioni di errore di trasformazione controllano quali errori vengono eliminati quando viene applicata la trasformazione. Le condizioni di errore incluse nella trasformazione vengono sostituite dalle condizioni di errore specificate usando i [**metodi MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) [**e ApplyTransform.**](database-applytransform.md)

> [!Note]  
> Le trasformazioni di personalizzazione tipiche non hanno condizioni di convalida o vengono convalidate in base a [**ProductCode.**](productcode.md) Le trasformazioni archiviate all'interno [dei pacchetti di patch](patch-packages.md) hanno in genere condizioni di convalida rigorose per garantire che alla destinazione della patch sia applicata la trasformazione corretta.

 

Esistono tre tipi di trasformazioni Windows installer:

-   [Trasformazioni incorporate](embedded-transforms.md)
-   [Trasformazioni protette](secured-transforms.md)
-   [Trasformazioni non protette](unsecured-transforms.md)

 

 



