---
description: Attenersi alle linee guida seguenti quando si crea una patch per un piccolo Windows programma di installazione.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Creazione di una patch di aggiornamento di piccole dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2c3dffac099358b924914b5dbd86871ba370241c42a2e3fd5caef2d8f12ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379396"
---
# <a name="creating-a-small-update-patch"></a>Creazione di una patch di aggiornamento di piccole dimensioni

Quando si crea una patch per [gli aggiornamenti di piccole dimensioni,](small-updates.md)gli autori devono rispettare le linee guida seguenti:

-   Le patch di aggiornamento di piccole dimensioni devono essere progettate per una singola installazione di destinazione.
-   Le patch di aggiornamento di piccole dimensioni devono usare la versione meno recente come installazione di destinazione.
-   Una patch di aggiornamento di piccole dimensioni deve sostituire e rendere obsolete tutte le patch di aggiornamento di piccole dimensioni precedenti.

Lo scenario seguente illustra quando è ottimale una patch di aggiornamento di piccole dimensioni.

La società viene fornita la versione 1.0 di Myproduct.msi. Poco dopo, si spedirà una [piccola](small-updates.md) patch di aggiornamento per Myproduct.msi denominata QFE1. Questa operazione non modifica la [**proprietà ProductCode**](productcode.md) o [**la proprietà ProductVersion.**](productversion.md)

Successivamente, si crea una seconda [patch di aggiornamento di](small-updates.md) piccole dimensioni per Myproduct.msi denominata QFE2. Questa seconda patch deve essere Myproduct.msi versione 1.0. Questa seconda patch non deve essere Myproduct.msi versione 1.0 e Myproduct.msi versione 1.0 + QFE1. Quando si applica QFE2, deve rimuovere QFE1.

 

 



