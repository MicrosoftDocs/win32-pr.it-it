---
description: Usare queste linee guida per creare un pacchetto Windows Installer che contiene più di 32767 file.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Creazione di un pacchetto di grandi dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d55f7933fe600bd6c0db0705328f18d7eae2f55e3463e3ea03be8118229eca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996881"
---
# <a name="authoring-a-large-package"></a>Creazione di un pacchetto di grandi dimensioni

Usare queste linee guida per creare un pacchetto Windows Installer che contiene più di 32767 file.

Se il pacchetto Windows Installer contiene più di 32767 file, è necessario modificare lo schema del database per aumentare il limite delle colonne seguenti:

-   Colonna Sequenza della tabella [File](file-table.md).
-   Colonna LastSequence della tabella [Media](media-table.md).
-   Colonna Sequenza della tabella [Patch](patch-table.md).

Per altre informazioni, vedere [Formato definizione colonna.](column-definition-format.md)

**Per aumentare il limite di una colonna di database**

1.  Esportare la tabella in un file con estensione idt. Per informazioni dettagliate, [vedereMsidb.exe](msidb-exe.md), Export [Files (Esportazione di file)](export-files.md) [e Importing and Exporting (Importazione ed esportazione).](importing-and-exporting.md)
2.  Modificare il file con estensione idt per modificare il tipo di colonna da i2 a i4 o da I2 a I4.
3.  Esportare [ \_ la tabella](-validation-table.md) Validation in un file con estensione idt.
4.  Modificare il file con estensione idt per modificare i valori nella colonna MaxValue della tabella [ \_ Validation](-validation-table.md) in modo da contenere l'aumento della larghezza delle colonne.
5.  Importare di nuovo i file con estensione idt nel database.

Si noti che non è possibile creare trasformazioni e patch tra due pacchetti con tipi di colonna diversi.

 

 



