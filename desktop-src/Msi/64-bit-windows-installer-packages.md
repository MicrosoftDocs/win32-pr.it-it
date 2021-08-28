---
description: Un pacchetto a 64 bit è costituito parzialmente o interamente da componenti Windows installer a 64 bit.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: Pacchetti del programma di Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540ef7afc5c70eeba2bb24eb376eae8e52b8e55cec2c8622ccdcf18a804b6f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559541"
---
# <a name="64-bit-windows-installer-packages"></a>Pacchetti del programma di Windows a 64 bit

Un pacchetto a 64 bit è costituito parzialmente o interamente da componenti Windows [installer](windows-installer-components.md) a 64 bit. L'elenco seguente identifica i requisiti per ogni pacchetto Windows installer a 64 bit:

-   Il valore "Intel64" deve essere immesso nel campo della piattaforma della proprietà [**Riepilogo**](template-summary.md) modello se e solo se il pacchetto viene eseguito su un processore Intel64 (Itanium).
-   Il valore "x64" deve essere immesso nel campo platform della proprietà [**Riepilogo**](template-summary.md) modello se e solo se il pacchetto viene eseguito su un processore x64.
-   Il valore "Arm64" deve essere immesso nel campo platform della proprietà [**Riepilogo**](template-summary.md) modello se e solo se il pacchetto viene eseguito in un processore Arm64.
-   La proprietà [**Riepilogo**](page-count-summary.md) conteggio pagine deve essere impostata sul numero intero 200 o versione successiva, perché il programma di installazione di Windows 2.0 è la versione minima in grado di installare componenti a 64 bit. I pacchetti per la piattaforma Arm64 richiedono un valore pari o superiore a 500.
-   Ogni componente Windows Installer a 64 bit nel pacchetto deve includere il bit **msidbComponentAttributes64bit** nella colonna Attributi della [tabella dei componenti](component-table.md).

Per altre informazioni, vedere [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md) and [32-bit Windows Installer Packages](32-bit-windows-installer-packages.md).

 

 



