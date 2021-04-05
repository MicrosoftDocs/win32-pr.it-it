---
description: Attenersi a queste linee guida durante la creazione di un modulo merge a 64 bit.
ms.assetid: 326c274b-981e-4b21-a4fb-0060c178a01e
title: Uso di moduli unione a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bfeec3f77e497fac0686cd6aeb44b69e987655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757805"
---
# <a name="using-64-bit-merge-modules"></a>Uso di moduli unione a 64 bit

Un modulo merge a 64 bit ha una delle caratteristiche identificate in questo argomento.

-   Il modulo merge contiene almeno un componente compilato per i sistemi operativi a 64 bit.
-   Il modulo merge non contiene componenti a 64 bit, ma deve essere utilizzato solo con i pacchetti [Windows Installer a 64 bit](64-bit-windows-installer-packages.md) .

I moduli merge possono essere usati come indicato di seguito:

-   Un modulo merge a 64 bit può essere unito in un pacchetto di [Windows Installer a 64 bit](64-bit-windows-installer-packages.md) . Le proprietà di [**Riepilogo del modello**](template-summary.md) nel modulo merge e nel pacchetto di Windows Installer devono essere impostate sullo stesso tipo di processore a 64 bit. Un modulo merge x64 può essere Unito solo a pacchetti x64 e un modulo merge Intel64 può essere Unito solo in pacchetti Intel64.
-   Un modulo merge a 32 bit può essere unito in pacchetti Windows Installer a 32 bit o [64 bit](64-bit-windows-installer-packages.md) .
-   Un modulo merge a 64 bit può essere unito in un pacchetto a 64 bit in un sistema operativo a 32 bit.

Quando si crea un modulo unione a 64 bit, attenersi alla seguente procedura:

-   Utilizzare la stessa procedura generale utilizzata per la creazione di moduli unione a 32 bit. Per informazioni, vedere [About merge modules](about-merge-modules.md) e [Authoring merge modules](authoring-merge-modules.md).
-   È necessario impostare la proprietà di [**Riepilogo del modello**](template-summary.md) con il valore Intel64 se si esegue un sistema Intel64. È necessario impostare la proprietà di **Riepilogo del modello** con il valore x64 se si esegue un sistema x64. Per informazioni, vedere [riferimento al flusso di informazioni di riepilogo del modulo merge](merge-module-summary-information-stream-reference.md).
-   Quando per lo stesso componente esistono entrambi i moduli unione a 32 bit e a 64 bit, è consigliabile che i moduli dispongano di firme diverse. Questo consentirà a un pacchetto di contenere entrambe le versioni del componente.

Per ulteriori informazioni, vedere [Windows Installer nei sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md).

 

 



