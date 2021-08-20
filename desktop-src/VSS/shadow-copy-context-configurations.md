---
description: I richiedenti controllano le funzionalità di una copia shadow impostandone il contesto. Questo contesto indica se la copia shadow non sarà più presente nell'operazione corrente e il grado di coordinamento tra writer e provider.
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: Configurazioni del contesto della copia shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e156b0357813060adcc3e7e8b5072b7a17543b7c996db72686a4912f504fede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937763"
---
# <a name="shadow-copy-context-configurations"></a>Configurazioni del contesto della copia shadow

I richiedenti controllano le funzionalità di una copia shadow impostandone il contesto. Questo contesto indica se la copia shadow non sarà più presente nell'operazione corrente e il grado di coordinamento tra writer e provider.

## <a name="persistence-and-shadow-copy-context"></a>Persistenza e contesto della copia shadow

Una copia shadow può essere [*persistente,*](vssgloss-p.md)ovvero la copia shadow non viene eliminata dopo la chiusura di un'operazione di backup o il rilascio di un [**oggetto IVssBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)

Le copie shadow permanenti richiedono contesti DI CONTESTO SNAPSHOT [**\_ VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) di **VSS \_ CTX \_ CLIENT \_ ACCESSIBLE,** ROLLBACK DELL'APP **VSS \_ CTX \_ \_** o **ROLLBACK NAS \_ \_ VSS \_ CTX.** Le copie shadow permanenti possono essere effettuate solo per i volumi NTFS.

Le copie shadow non costanti vengono create con i contesti di **VSS \_ CTX \_ BACKUP** o **VSS \_ CTX \_ FILE SHARE \_ \_ BACKUP**. È possibile creare copie shadow non per i volumi NTFS e non NTFS.

## <a name="writer-participation-and-shadow-copies"></a>Partecipazione al writer e copie shadow

Un contesto di copia shadow può essere classificato come che interessa o meno writer.

I contesti di copia shadow che coinvolgono gli autori nella creazione includono:

-   **ROLLBACK \_ DELL'APP VSS CTX \_ \_**
-   **VSS \_ CTX \_ BACKUP**
-   **WRITER ACCESSIBILI \_ DEL CLIENT VSS CTX \_ \_ \_**

Quelli che non coinvolgono gli autori nella loro creazione includono:

-   **CLIENT \_ VSS CTX \_ \_ ACCESSIBILE**
-   **BACKUP DI \_ CONDIVISIONE FILE VSS CTX \_ \_ \_**
-   **VSS \_ CTX \_ NAS \_ ROLLBACK**

Un contesto può essere usato con entrambi i tipi di copie shadow, ma non nella creazione di una copia shadow:

-   **VSS \_ CTX \_ ALL**

La creazione di una copia shadow con un contesto **di VSS \_ CTX \_ ALL** (con [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) e [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) non è supportata.

Le operazioni che supportano un contesto di **VSS \_ CTX \_ ALL** sono le operazioni amministrative [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::D eleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)e [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).

## <a name="obtaining-shadow-copy-information"></a>Recupero di informazioni sulla copia shadow

Se un richiedente conosce il GUID di identificazione di una copia shadow **\_ (il relativo ID VSS),** può ottenere informazioni sul contesto di una copia shadow specifica (identificata dal relativo **\_ ID VSS)** decomprimendo la struttura [**VSS \_ SNAPSHOT \_ PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) restituita da una chiamata a [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).

Per ottenere informazioni di contesto su tutte le copie shadow in un sistema, un richiedente esamina il membro **m \_ lSnapshotAttributes** del membro **Obj.Snap** della struttura [**VSS \_ OBJECT \_ PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (che è una struttura [**VSS SNAPSHOT \_ \_ PROP)**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ottenuto usando [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) per scorrere l'elenco di oggetti restituito da una chiamata a [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).

 

 



