---
description: Gestione degli errori di amministrazione COM+
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Gestione degli errori di amministrazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e5838d7fee7616a23f5e361df1aef65421492
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304950"
---
# <a name="handling-com-administration-errors"></a>Gestione degli errori di amministrazione COM+

Gli errori generati quando si utilizzano gli oggetti COMAdmin vengono segnalati in due modi, come indicato di seguito:

-   Utilizzo di codici di errore specifici della libreria COMAdmin.
-   Uso delle informazioni estese sull'errore disponibili in una raccolta [**errorInfo**](errorinfo.md) speciale.

## <a name="error-codes"></a>Codici errore

I codici di errore di amministrazione vengono gestiti come tutti i messaggi di errore COM. In Microsoft Visual C++, questi codici vengono restituiti come valori **HRESULT** . In Microsoft Visual Basic vengono generate come eccezioni che è possibile intercettare. Per i programmatori C++, i codici di errore di amministrazione COM+ sono definiti in Winerror. h. Per i programmatori Visual Basic, sono disponibili tramite l'IDE di Visual Basic.

## <a name="errorinfo-collection"></a>Raccolta ErrorInfo

Quando si verifica un errore, segnalato da un tipo di codice di errore, potrebbero essere disponibili informazioni più dettagliate, a seconda della natura dell'errore. Gli oggetti COMAdmin forniscono informazioni estese nei casi in cui la ragione precisa dell'errore è difficile da determinare senza un report dettagliato, ad esempio con più operazioni di lettura e scrittura.

Ad esempio, quando si usano metodi quali [**popolare**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) in un oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , è possibile leggere o scrivere dati per ogni elemento della raccolta. Possono verificarsi errori complessi e possono essere difficili da diagnosticare in base a un singolo codice di errore numerico. Pertanto, la libreria COMAdmin crea informazioni estese sugli errori tramite una raccolta speciale.

Quando sono disponibili informazioni estese sugli errori, questo viene inserito nella raccolta [**errorInfo**](errorinfo.md) correlata alla raccolta originale in cui si è verificato l'errore. Per recuperare la segnalazione errori, ottenere la raccolta **errorInfo** correlata alla raccolta originale ed esaminare gli elementi che contiene. È possibile recuperare la raccolta **errorInfo** usando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) in [**COMAdminCatalogCollection**](comadmincatalogcollection.md), lasciando vuoto il secondo parametro, dove normalmente si specifica la proprietà chiave di un elemento padre.

Quando viene ricevuto un errore, è necessario ottenere immediatamente e popolare la raccolta [**errorInfo**](errorinfo.md) per la raccolta che ha avuto esito negativo, senza eseguire altre operazioni su tale raccolta. In caso contrario, la raccolta **errorInfo** viene reimpostata e non descrive in dettaglio l'errore.

Gli elementi nella raccolta [**errorInfo**](errorinfo.md) espongono le proprietà speciali per la segnalazione degli errori MajorRef e MinorRef, che descrivono in dettaglio la particolare origine dell'errore. Per ulteriori informazioni, vedere **errorInfo**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operazioni di amministrazione COM+ all'interno delle transazioni](com--administration-operations-within-transactions.md)
</dt> <dt>

[Esempio introduttivo di utilizzo del catalogo di amministrazione COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Panoramica degli oggetti COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



