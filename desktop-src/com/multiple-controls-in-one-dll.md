---
title: Più controlli in una DLL
description: Più controlli in una DLL
ms.assetid: 76c1c0ef-af24-43e8-b3a7-337841c338ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b571f307f3438ca8f8ce0a0a716af2042884520cd07746f8e6fa8c1739fae22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130063"
---
# <a name="multiple-controls-in-one-dll"></a>Più controlli in una DLL

Una singola DLL con estensione ocx può contenere un numero qualsiasi di ActiveX, semplificando così la distribuzione e l'uso di un set di controlli correlati.

Se si spedisci più controlli in una singola DLL, assicurati di includere il nome del fornitore in ogni nome di controllo nel pacchetto. L'inclusione dei nomi dei fornitori in ogni nome di controllo consentirà agli utenti di identificare facilmente i controlli all'interno di un pacchetto. Ad esempio, se si spedi una DLL che implementa tre controlli, Con1, Con2 e Con3, i nomi dei controlli devono essere:

-   *Nome della società* Controllo Con1

-   *Nome della società* Controllo Con2

-   *Nome della società* Controllo Con3

 

 




