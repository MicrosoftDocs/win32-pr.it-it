---
title: Più controlli in una DLL
description: Più controlli in una DLL
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e11c91faa26420f37df330ad7f1d9eff4587f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044146"
---
# <a name="multiple-controls-in-one-dll"></a>Più controlli in una DLL

Una singola DLL OCX può comportare un numero qualsiasi di controlli ActiveX, semplificando in tal modo la distribuzione e l'utilizzo di un set di controlli correlati.

Se si distribuiscono più controlli in una singola DLL, assicurarsi di includere il nome del fornitore in ogni nome di controllo nel pacchetto. L'inclusione dei nomi dei fornitori in ogni nome di controllo consentirà agli utenti di identificare facilmente i controlli all'interno di un pacchetto. Se, ad esempio, si invia una DLL che implementa tre controlli, con1, CON2 e con3, i nomi dei controlli devono essere:

-   *Nome della società* Controllo con1

-   *Nome della società* Controllo con2

-   *Nome della società* Controllo con3

 

 




