---
description: Utilizzare queste linee guida per creare un pacchetto di Windows Installer contenente più di 32767 file.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Creazione di un pacchetto di grandi dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca09c427336e4ca8a17fd8ebdf803f52ebe6c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311046"
---
# <a name="authoring-a-large-package"></a>Creazione di un pacchetto di grandi dimensioni

Utilizzare queste linee guida per creare un pacchetto di Windows Installer contenente più di 32767 file.

Se il pacchetto di Windows Installer contiene più di 32767 file, è necessario modificare lo schema del database per aumentare il limite delle colonne seguenti:

-   Colonna sequenza della tabella dei [file](file-table.md).
-   Colonna LastSequence della tabella dei [supporti](media-table.md).
-   Colonna sequenza della tabella delle [patch](patch-table.md).

Per altre informazioni, vedere [formato della definizione di colonna](column-definition-format.md).

**Per aumentare il limite di una colonna del database**

1.  Esportare la tabella in un file con estensione IDT. Per informazioni dettagliate, vedere [Msidb.exe](msidb-exe.md), [esportare file](export-files.md), [importazione ed esportazione](importing-and-exporting.md).
2.  Modificare il file con estensione IDT per modificare il tipo di colonna da i2 a I4 o da i2 a i4.
3.  Esportare la tabella di [ \_ convalida](-validation-table.md) in un file con estensione IDT.
4.  Modificare il file con estensione IDT per modificare i valori nella colonna MaxValue della tabella di [ \_ convalida](-validation-table.md) in modo da includere la larghezza delle colonne aumentata.
5.  Importare di nuovo i file con estensione IDT nel database.

Si noti che non è possibile creare trasformazioni e patch tra due pacchetti con tipi di colonne diversi.

 

 



