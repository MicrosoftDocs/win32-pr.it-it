---
description: I writer possono ottimizzare le prestazioni di vari tipi di backup a livello di set di file indicando tramite un tipo di backup della specifica di file, indicato da una maschera di bit o da OR bit per bit dei membri dell'enumerazione VSS \_ FILE \_ SPEC BACKUP \_ \_ TYPE.
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Supporto dello schema a livello di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550885a540e62fc145541bae979fad34cb9488f62f9f26ea17e647068c1fad46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006371"
---
# <a name="file-level-schema-support"></a>Supporto dello schema a livello di file

I writer possono ottimizzare le prestazioni di vari tipi di backup a livello di [*set*](vssgloss-f.md) di file indicando tramite un tipo di backup della specifica di file, indicato da una maschera di bit o da OR bit per bit dei membri dell'enumerazione [**VSS FILE SPEC BACKUP \_ \_ \_ \_ TYPE.**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)

Per i tipi di backup specificati, il writer indica quanto segue:

-   Indica se sarà necessario eseguire la copia shadow del volume per eseguire correttamente il backup di un set di file. Ad esempio, se i file in un set di file non vengono aperti esclusivamente dal writer e possono garantire che sia stabile, non è necessaria una copia shadow.
-   Se il richiedente deve eseguire il backup in modo che, indipendentemente dall'ora dell'ultima modifica o da altri problemi, verrà ripristinata la versione dei file del set di file corrente durante il backup. Ciò significa in genere che il set di file viene copiato come parte del backup.

I valori di [**VSS \_ FILE SPEC BACKUP TYPE \_ \_ \_ che**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) indicano il requisito della copia shadow sono:

-   VSS \_ FSBT \_ ALL \_ SNAPSHOT \_ REQUIRED
-   VSS \_ FSBT \_ FULL \_ SNAPSHOT \_ REQUIRED
-   È NECESSARIO UNO SNAPSHOT DIFFERENZIALE DI VSS \_ FSBT \_ \_ \_
-   SNAPSHOT INCREMENTALE DI VSS \_ FSBT \_ \_ \_ OBBLIGATORIO
-   SNAPSHOT DEL LOG FSBT DI VSS \_ \_ \_ \_ OBBLIGATORIO

I valori di [**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) che indicano la necessità di eseguire il backup di un file sono:

-   VSS \_ FSBT \_ ALL \_ BACKUP \_ REQUIRED
-   BACKUP COMPLETO DI VSS \_ FSBT \_ \_ \_ OBBLIGATORIO
-   BACKUP DIFFERENZIALE DI VSS \_ FSBT \_ \_ \_ OBBLIGATORIO
-   BACKUP INCREMENTALE DI VSS \_ FSBT \_ \_ \_ OBBLIGATORIO
-   BACKUP DEL LOG FSBT DI VSS \_ \_ \_ \_ OBBLIGATORIO

Per impostazione predefinita, i set di file sono contrassegnati con un tipo di backup della specifica di file DI VSS \_ FSBT \_ ALL BACKUP REQUIRED \_ \_ \| VSS \_ FSBT \_ ALL SNAPSHOT REQUIRED, \_ \_ vale a dire che è sempre necessaria una copia shadow per gestire i file del set di file e che i file devono essere copiati in tutti i tipi di backup.

 

 



