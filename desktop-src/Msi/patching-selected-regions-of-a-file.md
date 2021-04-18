---
description: Quando si applica l'applicazione di patch ai file con contenuto variabile, potrebbe essere necessario mantenere le aree selezionate del file di destinazione per impedire la perdita di informazioni critiche.
ms.assetid: 4a610588-556e-489f-ac14-73e5e6b776fe
title: Applicazione di patch alle aree selezionate di un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778df4b0cc98eeacd1106929b18c7461c6fa9e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308892"
---
# <a name="patching-selected-regions-of-a-file"></a>Applicazione di patch alle aree selezionate di un file

Quando si applica l'applicazione di patch ai file con contenuto variabile, potrebbe essere necessario mantenere le aree selezionate del file di destinazione per impedire la perdita di informazioni critiche. Alcune applicazioni, ad esempio, timbrano le informazioni utente nel file eseguibile. Poiché il contenuto del file di destinazione può dipendere dal computer in cui è installata l'applicazione, diventa difficile determinare se un file specifico è una destinazione valida per la patch. Le informazioni sugli utenti scritte nel file di destinazione possono anche essere sovrascritte da una patch.

Quando si genera un file PCP (Patch Creation Properties) con [Msimsp.exe](msimsp-exe.md) e [PATCHWIZ.DLL](patchwiz-dll.md), è possibile specificare che le informazioni in determinate aree del file di destinazione vengano ignorate durante l'applicazione di patch. È anche possibile specificare che le informazioni in altre aree del file di destinazione vengano conservate e copiate in un percorso di offset nel file aggiornato. Specificare le aree del file di destinazione da ignorare e le aree da mantenere durante la creazione delle tabelle [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md), [ExternalFiles](externalfiles-table-patchwiz-dll-.md)e [FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md) .

Utilizzare la colonna RetainOffsets della tabella [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md) e le colonne RetainOffsets e RetainLengths della tabella [FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md) per copiare un intervallo di informazioni dal file di destinazione in un intervallo di offset nel file aggiornato. Le informazioni contenute in questo intervallo vengono mantenute. Consente di specificare la lunghezza dell'intervallo utilizzando le colonne RetainLengths della tabella FamilyFileRanges. La lunghezza dell'intervallo mantenuto è la stessa nei file di destinazione e aggiornati. Specificare l'offset dell'intervallo nel file di destinazione usando la colonna RetainOffsets della tabella TargetFiles OptionalData. Specificare l'offset dell'intervallo nel file aggiornato utilizzando la colonna RetainOffsets della tabella FamilyFileRanges. L'intervallo del file di destinazione mantenuto è quindi il valore di RetainOffsets nella tabella TargetFiles OptionalData e RetainLengths. Queste informazioni vengono copiate nel file di aggiornamento nell'intervallo specificato dal valore di RetainOffsets nelle tabelle FamilyFileRanges più RetainLengths. È possibile specificare più intervalli, ma l'ordine delle lunghezze deve corrispondere all'ordine degli offset.

Usare la tabella [TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md) per ignorare un intervallo del file di destinazione. Le informazioni contenute in questo intervallo del file di destinazione possono comunque essere sovrascritte dalla patch. Specificare l'offset dell'intervallo nella colonna IgnoreOffsets e la relativa lunghezza nella colonna IgnoreLengths. È possibile specificare più intervalli, ma l'ordine delle lunghezze deve corrispondere all'ordine degli offset.

I valori nelle colonne lunghezze e offset possono essere decimali o esadecimali. [PATCHWIZ.DLL](patchwiz-dll.md) considera il valore come esadecimale se è preceduto da "0x". Le colonne sono colonne stringa, quindi PATCHWIZ.DLL converte i valori in ULONG. La colonna length specifica la lunghezza in byte.

 

 



