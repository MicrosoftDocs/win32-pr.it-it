---
description: Salvataggio o rimozione delle modifiche
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Salvataggio o rimozione delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01c000a6fc9fbe7e8e25e50c041f1b5a0e1250dfe089245ef035213905e5737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915932"
---
# <a name="saving-or-discarding-changes"></a>Salvataggio o rimozione delle modifiche

Quando si impostano le proprietà per un elemento, nessuna modifica viene effettivamente registrata nel catalogo COM+ fino a quando non si salvano in modo esplicito le modifiche. A tale scopo, usare [**il metodo SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) nell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) per la raccolta contenente l'elemento.

Se si desidera annullare le modifiche di cui non è ancora stato eseguito il commit, è possibile chiamare il metodo [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) [**sull'oggetto COMAdminCatalogCollection.**](comadmincatalogcollection.md) Questa operazione legge tutti i dati persistenti dal catalogo COM+ per tutti gli elementi nella raccolta, eliminando in modo efficace eventuali modifiche in sospeso.

Quando si usa [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), eventuali incoerenze nelle impostazioni delle proprietà scelte causano un errore e **SaveChanges** non riesce a scrivere l'oggetto che ha restituito l'errore. Tutte le proprietà di un determinato elemento vengono scritte o non vengono scritte nel loro insieme.

Tuttavia, quando si verificano errori di scrittura, potrebbero non essere dovuti a impostazioni incompatibili. è possibile che si sia verificato un altro errore. È necessario esaminare i dettagli dell'errore per essere certi. Per altre informazioni, vedere [Gestione di errori di amministrazione COM+](handling-com--administration-errors.md) e [Interdipendenze tra proprietà.](interdependencies-between-properties.md)

Come regola generale, maggiore è il numero di modifiche che si tenta di salvare contemporaneamente, in particolare le modifiche a più oggetti, maggiore è la probabilità che si otterrà un errore e più difficile sarà il rilevamento.

Inoltre, tra le chiamate a [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), non è presente un blocco sugli elementi nella raccolta. è possibile una contention. Per altri dettagli, vedere [Recupero e impostazione delle proprietà.](getting-and-setting-properties.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Recupero e impostazione delle proprietà](getting-and-setting-properties.md)
</dt> <dt>

[Interdipendenze tra proprietà](interdependencies-between-properties.md)
</dt> <dt>

[Esecuzione di query per le proprietà disponibili](querying-for-available-properties.md)
</dt> </dl>

 

 



