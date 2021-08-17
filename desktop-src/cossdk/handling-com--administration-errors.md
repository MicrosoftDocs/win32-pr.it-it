---
description: Gestione degli errori di amministrazione COM+
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Gestione degli errori di amministrazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 965276fff68edf45ae27423ee4ed707e4bb7f1476b0237dab270538e0fa0f1be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306709"
---
# <a name="handling-com-administration-errors"></a>Gestione degli errori di amministrazione COM+

Gli errori generati quando si usano gli oggetti COMAdmin vengono segnalati in due modi, come indicato di seguito:

-   Uso di codici di errore specifici della libreria COMAdmin.
-   Uso delle informazioni estese sugli errori disponibili in una raccolta [**ErrorInfo**](errorinfo.md) speciale.

## <a name="error-codes"></a>Codici errore

I codici di errore di amministrazione vengono gestiti come qualsiasi messaggio di errore COM. In Microsoft Visual C++ questi codici vengono restituiti come **valori HRESULT.** In Microsoft Visual Basic vengono generate come eccezioni che è possibile rilevare. Per i programmatori C++, i codici di errore di amministrazione COM+ sono definiti in Winerror.h. Per Visual Basic programmatori, sono disponibili tramite l'IDE Visual Basic.

## <a name="errorinfo-collection"></a>Raccolta ErrorInfo

Quando si verifica un errore, segnalato da un tipo di codice di errore, potrebbero essere disponibili informazioni più dettagliate, a seconda della natura dell'errore. Gli oggetti COMAdmin forniscono informazioni estese nei casi in cui la causa precisa dell'errore è difficile da determinare senza un report dettagliato, ad esempio con più operazioni di lettura e scrittura.

Ad esempio, quando si usano metodi come [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) in un oggetto [**COMAdminCatalogCollection,**](comadmincatalogcollection.md) è possibile leggere o scrivere dati per ogni elemento della raccolta. Possono verificarsi errori complessi e possono essere difficili da diagnosticare in base a un singolo codice di errore numerico. Di conseguenza, la libreria COMAdmin rende le informazioni sugli errori estese tramite una raccolta speciale.

Quando sono disponibili informazioni sugli errori estesi, vengono inserite nella raccolta [**ErrorInfo**](errorinfo.md) correlata alla raccolta originale in cui si è verificato l'errore. Per recuperare la segnalazione errori, ottenere la raccolta **ErrorInfo** correlata alla raccolta originale ed esaminare gli elementi in essa contenuti. È possibile recuperare la **raccolta ErrorInfo** usando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) in [**COMAdminCatalogCollection,**](comadmincatalogcollection.md)lasciando vuoto il secondo parametro in cui normalmente si specifica la proprietà Key di un elemento padre.

Quando si verifica un errore, è necessario ottenere e popolare immediatamente la raccolta [**ErrorInfo**](errorinfo.md) per la raccolta non riuscita, senza eseguire altre operazioni su tale raccolta. In caso contrario, la **raccolta ErrorInfo** viene reimpostata e non indica in dettaglio l'errore.

Gli elementi nella raccolta [**ErrorInfo**](errorinfo.md) espongono le proprietà speciali di segnalazione errori MajorRef e MinorRef, che specificano in dettaglio la causa specifica dell'errore. Per altre informazioni, vedere **ErrorInfo**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operazioni di amministrazione COM+ all'interno delle transazioni](com--administration-operations-within-transactions.md)
</dt> <dt>

[Esempio introduttivo sull'uso del catalogo di amministrazione COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Panoramica degli oggetti COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



