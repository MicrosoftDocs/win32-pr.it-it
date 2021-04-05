---
title: Creazione di oggetti collegati e incorporati da dati esistenti
description: Creazione di oggetti collegati e incorporati da dati esistenti
ms.assetid: 76848b7e-6068-4bac-9793-304f813096f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f60064516a4312a9de3ce511e00e49ce7276f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714266"
---
# <a name="creating-linked-and-embedded-objects-from-existing-data"></a>Creazione di oggetti collegati e incorporati da dati esistenti

Un utente in genere assembla un documento composto usando gli Appunti o il trascinamento della selezione per copiare un oggetto dati dalla relativa applicazione server all'applicazione contenitore dell'utente. Con le applicazioni che supportano OLE, l'utente può avviare il trasferimento dal server o dal contenitore. Il server può, ad esempio, copiare i dati negli Appunti nell'applicazione server, quindi passare all'applicazione contenitore e scegliere Incolla oggetto speciale/incorporato o un comando di menu equivalente per creare un nuovo oggetto incorporato dai dati selezionati. In alternativa, l'utente può trascinare i dati da un'applicazione all'altra. Il processo è simile per la creazione di un oggetto collegato.

> [!Note]  
> Un'applicazione che funge sia da server OLE che da contenitore può utilizzare una selezione dei propri dati per creare un oggetto incorporato o collegato in una nuova posizione all'interno dello stesso documento.

 

Il trasferimento dei dati tra il server OLE e le applicazioni contenitore è basato sul trasferimento dati uniforme, come descritto in [trasferimento dati](data-transfer.md). I server OLE e i gestori di oggetti implementano [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) per rendere i dati disponibili per i trasferimenti usando gli Appunti o il trascinamento della selezione. Gli oggetti OLE supportano tutti i formati degli Appunti usuali. Sono inoltre supportati sei formati degli appunti che supportano la creazione di oggetti collegati e incorporati da un oggetto dati selezionato.

I formati degli Appunti OLE descrivono gli oggetti dati che, dopo essere stati eliminati o incollati nei contenitori OLE, devono diventare oggetti di documenti compositi incorporati o collegati. L'oggetto dati presenta questi formati alle applicazioni contenitore in ordine di fedeltà come descrizione dei dati. In altre parole, l'oggetto presenta innanzitutto il formato che meglio lo rappresenta, seguito dal formato migliore successivo e così via. Questo ordinamento intenzionale invita un'applicazione contenitore a usare il formato migliore possibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> <dt>

[Trasferimento dati](data-transfer.md)
</dt> </dl>

 

 




