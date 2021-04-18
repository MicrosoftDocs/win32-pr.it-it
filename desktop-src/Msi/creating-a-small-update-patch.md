---
description: Quando si crea una patch per un aggiornamento Windows Installer Small, attenersi alle linee guida seguenti.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Creazione di una patch di aggiornamento di piccole dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d948c871baed7fbc15545ed9669c9864ce954799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318288"
---
# <a name="creating-a-small-update-patch"></a>Creazione di una patch di aggiornamento di piccole dimensioni

Quando si crea una patch per [piccoli aggiornamenti](small-updates.md), gli autori devono rispettare le linee guida seguenti:

-   Le patch di aggiornamento di piccole dimensioni devono essere progettate per una singola installazione di destinazione.
-   Le patch di aggiornamento di piccole dimensioni devono usare la versione più recente dell'installazione di destinazione.
-   Una patch di aggiornamento di piccole dimensioni dovrebbe sostituire e rendere obsolete le patch di aggiornamento di piccole dimensioni precedenti.

Lo scenario seguente illustra quando è preferibile una patch di aggiornamento di dimensioni ridotte.

La società viene fornita dalla versione 1,0 del Myproduct.msi. Poco dopo, viene fornita una patch di [aggiornamento di piccole dimensioni](small-updates.md) per Myproduct.msi denominata QFE1. Questa operazione non comporta la modifica della proprietà [**ProductCode**](productcode.md) o della proprietà [**ProductVersion**](productversion.md) .

Successivamente, è possibile creare una seconda patch di [aggiornamento di piccole dimensioni](small-updates.md) per Myproduct.msi denominata QFE2. Questa seconda patch deve avere come destinazione Myproduct.msi versione 1,0. Questa seconda patch non deve essere destinata a Myproduct.msi versione 1,0 e Myproduct.msi versione 1,0 + QFE1. Quando QFE2 viene applicato, deve rimuovere QFE1.

 

 



