---
title: Replica della partizione di directory applicativa
description: Le partizioni di directory applicative vengono spesso utilizzate per archiviare i dati dinamici.
ms.assetid: b5fbec54-ee1a-4fe6-b4b7-67fc4e77d043
ms.tgt_platform: multiple
keywords:
- Active Directory della partizione di directory applicativa
- Directory dell'applicazione partizioni di Active Directory, replica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41523b86ae8d3a744d4eb288c5b240a60222aa21
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046560"
---
# <a name="application-directory-partition-replication"></a>Replica della partizione di directory applicativa

Le partizioni di directory applicative vengono spesso utilizzate per archiviare i dati dinamici. Poiché i dati vengono modificati più spesso rispetto ai dati di configurazione di una foresta, è possibile impostare l'ambito di replica e la frequenza di una partizione di directory applicativa per ogni partizione. È possibile utilizzare le funzionalità di replica di Active Directory Domain Services, ma è possibile ottimizzare i dati di replica in base al tipo di dati archiviati nella partizione.

Il sistema operativo non impone un numero massimo di repliche, ma il numero di repliche deve essere mantenuto come minimo per ridurre l'effetto sulle prestazioni della replica dei dati della partizione di directory applicativa dinamica.

KCC genera e mantiene la topologia di replica per una partizione di directory applicativa.

## <a name="application-directory-partition-replication-within-a-site"></a>Replica della partizione di directory applicativa all'interno di un sito

È possibile configurare gli intervalli di replica che controllano la replica all'interno del sito di una partizione di directory applicativa. Ciò consente di sincronizzare i dati dinamici in una partizione di directory applicativa più tempestivamente rispetto ai dati più statici in una partizione di dominio. Per ulteriori informazioni sulla configurazione di una partizione di directory applicativa a livello di codice, vedere [modifica della configurazione della partizione di directory applicativa](modifying-application-directory-partition-configuration.md).

Due attributi sull'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) della partizione di directory applicativa e due valori del registro di sistema in ogni controller di dominio Windows 2000 e versioni successive controllano la latenza di avvio di una notifica di modifica di origine ai partner di replica all'interno di un sito.

-   L'attributo [**msDS-Replication-Notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay) di un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) specifica il ritardo, in secondi, dopo la modifica di un oggetto di origine prima della notifica del primo partner di replica. Un valore del registro di sistema in ogni controller di dominio può specificare un valore simile. In una foresta di Windows Server 2003, il primo ritardo predefinito è 15 secondi. In una foresta in modalità mista, il primo ritardo predefinito è cinque minuti.
-   L'attributo [**msDS-Replication-Notify-susseguente-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) di un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) specifica il ritardo, in secondi, tra le notifiche successive e il secondo, il terzo e così via sui partner di replica. Un valore del registro di sistema in ogni controller di dominio può specificare un valore simile. In una foresta di Windows Server 2003, il ritardo successivo predefinito è di 3 secondi. In una foresta in modalità mista, il ritardo successivo predefinito è 30 secondi.

Gli attributi [**crossRef**](/windows/desktop/ADSchema/c-crossref) si applicano a tutti i controller di dominio che ospitano una replica della partizione di directory applicativa e influiscono solo sulla replica della partizione di directory applicativa identificata dall'oggetto **crossRef** . I valori del registro di sistema si applicano solo al controller di dominio in cui sono impostati e influiscono sulla replica all'interno del sito per tutte le partizioni ospitate dal controller di dominio. Se non vengono impostati né gli attributi **crossRef** né i relativi valori del registro di sistema, un controller di dominio utilizzerà i valori predefiniti. Se i valori del registro di sistema sono impostati, eseguono l'override di tutti i valori impostati nell'oggetto **crossRef** . Per impostazione predefinita, i valori del registro di sistema e **crossRef** non sono impostati, quindi vengono usati i valori predefiniti. Ciò consente a un amministratore di velocizzare la replica per tutte le repliche di una partizione di directory applicativa impostando i valori **crossRef** , abilitando allo stesso tempo l'ottimizzazione con le impostazioni del registro di sistema in ogni controller di dominio.

A partire da Windows Server 2003, le partizioni di dominio usano anche questi attributi dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) per controllare la latenza di replica all'interno del sito. Si tratta di una modifica rispetto alle versioni precedenti del server in cui gli intervalli di ritardo sono stati controllati dai valori del registro di sistema in ogni controller di dominio. Quando la foresta viene aggiornata a Windows Server 2003, i valori del registro di sistema esistenti vengono conservati solo se sono stati modificati rispetto ai valori predefiniti. Gli intervalli di notifica dei controller di dominio nel registro di sistema eseguono l'override degli intervalli di notifica archiviati nell'oggetto **crossRef** della partizione.

## <a name="application-directory-partition-replication-across-sites"></a>Replica della partizione di directory applicativa tra siti

Le repliche di una partizione di directory applicativa posizionata tra siti rispettano la pianificazione della replica tra siti, come per la partizione di dominio e la replica del catalogo globale. Tuttavia, le repliche di una partizione di directory applicativa sono più spesso situate all'interno di un sito quando ospitano dati realmente volatili perché la latenza di replica tra siti potrebbe non essere accettabile per ottenere le repliche coerenti tra loro.

## <a name="application-directory-partitions-are-not-replicated-to-global-catalogs"></a>Le partizioni di directory applicative non vengono replicate nei cataloghi globali

Gli oggetti in una partizione di directory applicativa non vengono replicati nel catalogo globale. La partizione di directory applicativa viene fornita come hosting di dati dinamici e oggetti per i quali potrebbe non essere ragionevole, né possibile replicare gli oggetti in modo esteso. Per questo motivo, la partizione di directory applicativa offre ambito controllato e frequenza di replica. Per questo motivo, non è necessario consentire la replica di questi oggetti nel catalogo globale e quindi essere distribuiti nell'intera foresta in cui è presente un server di catalogo globale. Questa operazione non impedisce agli oggetti in una partizione di directory applicativa di utilizzare gli attributi nello schema contrassegnato come [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset). Come con qualsiasi controller di dominio, un server di catalogo globale può comunque essere configurato come una replica completa di una partizione di directory applicativa.

 

 