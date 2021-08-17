---
title: Replica delle partizioni di directory applicative
description: Le partizioni di directory applicative vengono usate più spesso per archiviare i dati dinamici.
ms.assetid: b5fbec54-ee1a-4fe6-b4b7-67fc4e77d043
ms.tgt_platform: multiple
keywords:
- Replica della partizione di directory applicativa AD
- Partizioni di directory applicative AD , Replica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7df6c50653fe1660bbf95f0f6ca580404d38c366c1045bc3d1b712ca771d3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024411"
---
# <a name="application-directory-partition-replication"></a>Replica delle partizioni di directory applicative

Le partizioni di directory applicative vengono usate più spesso per archiviare i dati dinamici. Poiché i dati cambiano più spesso dei dati di configurazione per una foresta, è possibile impostare l'ambito di replica e la frequenza di una partizione di directory applicativa per ogni partizione. Le funzionalità di replica Active Directory Domain Services possono essere utilizzate, ma i dati di replica possono essere ottimizzati in base al tipo di dati archiviati nella partizione.

Il sistema operativo non impone un numero massimo di repliche, ma il numero di repliche deve essere mantenuto al minimo per ridurre l'impatto sulle prestazioni della replica dei dati dinamici della partizione di directory applicativa.

Il KCC genera e gestisce la topologia di replica per una partizione di directory applicativa.

## <a name="application-directory-partition-replication-within-a-site"></a>Replica della partizione di directory applicativa all'interno di un sito

È possibile configurare gli intervalli di replica che controllano la replica all'interno del sito di una partizione di directory applicativa. In questo modo i dati dinamici in una partizione di directory applicativa possono essere sincronizzati più tempestivamente rispetto ai dati più statici in una partizione di dominio. Per altre informazioni sulla configurazione di una partizione di directory applicativa a livello di codice, vedere [Modifica della configurazione della partizione di directory applicativa](modifying-application-directory-partition-configuration.md).

Due attributi nell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) della partizione di directory applicativa e due valori del Registro di sistema in ogni controller di dominio Windows 2000 e versioni successive controllano la latenza di avvio di una notifica di modifica di origine ai partner di replica all'interno di un sito.

-   L'attributo [**msDS-Replication-Notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay) di un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) specifica il ritardo, in secondi, dopo la modifica di un oggetto di origine prima della notifica del primo partner di replica. Un valore del Registro di sistema in ogni controller di dominio può specificare un valore simile. In una Windows server 2003 il primo ritardo predefinito è 15 secondi. In una foresta in modalità mista il primo ritardo predefinito è di cinque minuti.
-   [**L'attributo msDS-Replication-Notify-Subsequent-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) di un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) specifica il ritardo, in secondi, tra le notifiche successive ai partner di replica secondo, terzo e così via. Un valore del Registro di sistema in ogni controller di dominio può specificare un valore simile. In una Windows server 2003, il ritardo successivo predefinito è di 3 secondi. In una foresta in modalità mista il ritardo successivo predefinito è di 30 secondi.

Gli [**attributi crossRef**](/windows/desktop/ADSchema/c-crossref) si applicano a tutti i controller di dominio che ospitano una replica della partizione di directory applicativa e influiscono solo sulla replica della partizione di directory applicativa identificata dall'oggetto **crossRef.** I valori del Registro di sistema si applicano solo al controller di dominio in cui sono impostati e influiscono sulla replica all'interno del sito per tutte le partizioni ospitate dal controller di dominio. Se non sono **impostati né gli attributi crossRef** né i relativi valori del Registro di sistema, un controller di dominio usa i valori predefiniti. Se i valori del Registro di sistema sono impostati, eseguono l'override di tutti i valori impostati **nell'oggetto crossRef.** Per impostazione predefinita, i valori del Registro di sistema e **di crossRef** non sono impostati, quindi vengono usati i valori predefiniti. Ciò consente a un amministratore di velocizzare la replica per tutte le repliche di una partizione di directory applicativa impostando i **valori crossRef,** abilitando al tempo stesso un'ottimizzazione più fine con le impostazioni del Registro di sistema in ogni controller di dominio.

A partire da Windows Server 2003, le partizioni di dominio usano anche questi attributi dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) per controllare la latenza di replica all'interno del sito. Si tratta di una modifica rispetto alle versioni precedenti del server in cui gli intervalli di ritardo sono stati controllati dai valori del Registro di sistema in ogni controller di dominio. Quando la foresta viene aggiornata a Windows Server 2003, i valori del Registro di sistema esistenti vengono mantenuti solo se sono stati modificati dai valori predefiniti. Gli intervalli di notifica dei controller di dominio nel Registro di sistema sostituiscono gli intervalli di notifica archiviati **nell'oggetto crossRef della** partizione.

## <a name="application-directory-partition-replication-across-sites"></a>Replica della partizione di directory applicativa tra siti

Le repliche di una partizione di directory applicativa che si trovano tra siti osservano la pianificazione della replica tra siti, come avviene per la partizione di dominio e la replica del catalogo globale. Tuttavia, le repliche di una partizione di directory applicativa si trovano più spesso all'interno di un sito quando ospitano dati realmente volatili, perché la latenza di replica tra siti potrebbe non essere accettabile per ottenere che le repliche siano coerenti tra loro.

## <a name="application-directory-partitions-are-not-replicated-to-global-catalogs"></a>Le partizioni di directory applicative non vengono replicate nei cataloghi globali

Gli oggetti in una partizione di directory applicativa non vengono replicati nel catalogo globale. La partizione di directory applicativa viene immaginata come hosting di dati dinamici e oggetti per i quali potrebbe non essere sensata né fattibile replicare gli oggetti su larga parte. Per questo motivo, la partizione di directory applicativa offre ambito controllato e frequenza di replica. Per questo motivo, non esiste alcun motivo per consentire la replica di questi oggetti nel catalogo globale e quindi essere distribuiti nell'intera foresta in cui è presente un server di catalogo globale. Ciò non impedisce agli oggetti in una partizione di directory applicativa di usare attributi nello schema contrassegnato come [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset). Come per qualsiasi controller di dominio, un server di catalogo globale può comunque essere configurato come replica completa di una partizione di directory applicativa.

 

 