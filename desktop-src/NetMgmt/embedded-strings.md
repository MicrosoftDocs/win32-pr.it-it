---
title: Stringhe incorporate
description: Le strutture informative non conterranno stringhe incorporate. Ciò migliora l'allineamento delle strutture di informazioni e consente la flessibilità OEM nelle funzioni di base.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c71ed50971661f9ad06855024ecba2796f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711578"
---
# <a name="embedded-strings"></a>Stringhe incorporate

Le strutture informative non conterranno stringhe incorporate. Ciò migliora l'allineamento delle strutture di informazioni e consente la flessibilità OEM nelle funzioni di base.

Qualsiasi campo informazioni restituito in una chiamata di enumerazione che può essere successivamente usato come chiave per la chiamata a una funzione di gestione di rete GetInfo è sicuramente presente nel buffer di enumerazione. Se la stringa di informazioni a lunghezza variabile che specifica il valore del campo chiave non si adatta, non viene restituita l'intera struttura a lunghezza fissa per la voce. Altri campi a lunghezza variabile verranno restituiti come puntatore **null** per il caso in cui la stringa non è adatta.

 

 




