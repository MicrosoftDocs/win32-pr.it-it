---
description: Un pacchetto a 64 bit è costituito parzialmente o interamente da componenti Windows Installer a 64 bit.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: Pacchetti Windows Installer a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b34c8ff7ce4809dc44932cc8a5daa978b6ff66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881185"
---
# <a name="64-bit-windows-installer-packages"></a>Pacchetti Windows Installer a 64 bit

Un pacchetto a 64 bit è costituito parzialmente o interamente da componenti [Windows Installer](windows-installer-components.md) a 64 bit. L'elenco seguente identifica i requisiti per ogni pacchetto di Windows Installer a 64 bit:

-   Il valore "Intel64" deve essere immesso nel campo piattaforma della proprietà [**Riepilogo modello**](template-summary.md) , se e solo se il pacchetto viene eseguito in un processore Intel64 (Itanium).
-   Il valore "x64" deve essere immesso nel campo piattaforma della proprietà [**Riepilogo modello**](template-summary.md) , se e solo se il pacchetto viene eseguito in un processore x64.
-   Il valore "Arm64" deve essere immesso nel campo piattaforma della proprietà [**Riepilogo modello**](template-summary.md) , se e solo se il pacchetto viene eseguito in un processore Arm64.
-   È necessario impostare la proprietà [**Riepilogo conteggio pagine**](page-count-summary.md) sull'intero 200 o su un valore maggiore, perché Windows Installer 2,0 è la versione minima in grado di installare i componenti a 64 bit. I pacchetti per la piattaforma Arm64 richiedono un valore di 500 o superiore.
-   Ogni componente Windows Installer a 64 bit nel pacchetto deve includere il bit **msidbComponentAttributes64bit** nella colonna Attributes della [tabella Component](component-table.md).

Per ulteriori informazioni, vedere [Windows Installer nei sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md) e [pacchetti di Windows Installer a 32 bit](32-bit-windows-installer-packages.md).

 

 



