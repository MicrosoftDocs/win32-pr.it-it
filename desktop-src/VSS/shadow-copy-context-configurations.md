---
description: I richiedenti controllano le funzionalità di una copia shadow impostando il relativo contesto. Questo contesto indica se la copia shadow sopravviverà all'operazione corrente e il livello di coordinamento del writer o del provider.
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: Configurazioni del contesto per copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb41d0e2604dcf92d27f490175cdcbafd49822c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528698"
---
# <a name="shadow-copy-context-configurations"></a>Configurazioni del contesto per copie shadow

I richiedenti controllano le funzionalità di una copia shadow impostando il relativo contesto. Questo contesto indica se la copia shadow sopravviverà all'operazione corrente e il livello di coordinamento del writer o del provider.

## <a name="persistence-and-shadow-copy-context"></a>Persistenza e contesto della copia shadow

Una copia shadow può essere [*permanente*](vssgloss-p.md), ovvero la copia shadow non viene eliminata in seguito alla chiusura di un'operazione di backup o al rilascio di un oggetto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .

Le copie shadow permanenti richiedono contesti del [**\_ \_ \_ contesto dello snapshot VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) di **VSS \_ ctx \_ client \_ accessibili**, **\_ rollback dell' \_ app \_ VSS CTX** o **rollback del \_ \_ server \_ VSS CTX**. Le copie shadow permanenti possono essere eseguite solo per i volumi NTFS.

Le copie shadow non permanenti vengono create con i contesti del backup **VSS \_ ctx \_** o del **\_ \_ \_ \_ backup della condivisione file VSS CTX**. È possibile effettuare copie shadow non permanenti per i volumi NTFS e non NTFS.

## <a name="writer-participation-and-shadow-copies"></a>Partecipazione e copie shadow del writer

Un contesto di copia shadow può essere classificato come coinvolgimento di writer o senza coinvolgere i writer.

I contesti di copia shadow che coinvolgono i writer nella loro creazione includono:

-   **\_rollback dell' \_ app VSS CTX \_**
-   **BACKUP di VSS \_ ctx \_**
-   **\_ \_ writer accessibili del client VSS CTX \_ \_**

Quelli che non coinvolgono i writer nella loro creazione includono:

-   **\_client CTX \_ VSS \_ accessibile**
-   **\_backup della \_ \_ condivisione file VSS CTX \_**
-   **\_rollback del \_ Server VSS CTX \_**

Un contesto può essere utilizzato con entrambi i tipi di copie shadow, ma non può essere utilizzato per la creazione di una copia shadow:

-   **\_totale VSS CTX \_**

La creazione di una copia shadow con un contesto di **VSS \_ ctx \_ All** (using [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) e [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) non è supportata.

Le operazioni che supportano un contesto di **VSS \_ CTX sono \_ tutte** le operazioni [**amministrative IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::D Eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)e [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).

## <a name="obtaining-shadow-copy-information"></a>Recupero delle informazioni sulla copia shadow

Se un richiedente conosce il GUID di identificazione di una copia shadow (il relativo **\_ ID VSS**), può ottenere informazioni sul contesto di una copia shadow specifica (identificata dal **relativo \_ ID VSS**) decomprimendo la struttura di [**\_ \_ prop snapshot VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) restituita da una chiamata a [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).

Per ottenere informazioni di contesto su tutte le copie shadow di un sistema, un richiedente esamina il membro **\_ LSnapshotAttributes** di **obj. snap del membro obj. snap** della struttura [**\_ \_ prop dell'oggetto VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (ovvero una struttura di [**\_ \_ prop snapshot VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) ottenuta usando [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) per scorrere l'elenco di oggetti restituiti da una chiamata a [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).

 

 



