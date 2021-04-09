---
description: I writer possono ottimizzare le prestazioni dei vari tipi di backup a livello di set di file indicando tramite un tipo di backup delle specifiche di file, indicato da una maschera di bit o bit per bit dei membri dell' \_ enumerazione del tipo di backup delle specifiche del file VSS \_ \_ \_ .
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Supporto dello schema a livello di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460d256a3eaa016933e697687d05e26838c14ae2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968487"
---
# <a name="file-level-schema-support"></a>Supporto dello schema a livello di file

I writer possono ottimizzare le prestazioni dei vari tipi di backup a livello di [*set di file*](vssgloss-f.md) indicando tramite un tipo di backup delle specifiche di file, indicato da una maschera di bit o bit per bit dei membri dell'enumerazione del [**tipo di backup delle \_ specifiche del file \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) .

Per i tipi di backup specificati, il writer indica quanto segue:

-   Indica se sarà necessario eseguire la copia shadow del volume per eseguire correttamente il backup di un set di file. Ad esempio, se i file in un set di file non vengono aperti esclusivamente dal writer e possono garantire che sia stabile, non è necessaria una copia shadow.
-   Se il richiedente deve eseguire il backup in modo tale che, indipendentemente dall'ora dell'Ultima modifica o da altri problemi, la versione dei file del set di file corrente al backup verrà ripristinata. In genere, ciò significa che il set di file viene copiato come parte del backup.

I valori del [**\_ tipo di \_ \_ backup delle \_ specifiche del file VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) che indicano il requisito della copia shadow sono:

-   VSS \_ FSBT \_ tutti gli \_ snapshot \_ necessari
-   \_ \_ snapshot completo VSS \_ FSBT \_ necessario
-   \_ \_ snapshot differenziale FSBT VSS \_ \_ obbligatorio
-   \_ \_ snapshot incrementale FSBT \_ VSS \_ obbligatorio
-   \_snapshot del \_ log FSBT VSS \_ \_ obbligatorio

I valori del [**\_ tipo di \_ \_ backup delle \_ specifiche del file VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) che indicano la necessità di eseguire il backup di un file sono:

-   VSS \_ FSBT \_ tutti i \_ backup \_ necessari
-   \_ \_ backup completo VSS \_ FSBT \_ obbligatorio
-   è \_ \_ necessario il \_ backup DIFFERENZIAle FSBT VSS \_
-   è \_ \_ necessario il backup incrementale FSBT VSS \_ \_
-   \_backup del \_ log FSBT VSS \_ \_ obbligatorio

Per impostazione predefinita, i set di file sono contrassegnati con un tipo di backup della specifica del file VSS \_ FSBT \_ tutti i \_ backup \_ necessari \| VSS \_ FSBT \_ tutti gli \_ snapshot \_ necessari, ovvero una copia shadow è sempre necessaria per gestire i file del set di file e che i file devono essere copiati in tutti i tipi di backup.

 

 



