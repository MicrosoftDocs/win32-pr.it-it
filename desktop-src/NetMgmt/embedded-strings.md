---
title: Stringhe incorporate
description: Le strutture di informazioni non conterranno stringhe incorporate. Ciò migliora l'allineamento delle strutture di informazioni e consente la flessibilità OEM nelle funzioni principali.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6121e805a1dbe329cee52a760c809ded21f1740b19adaa3e18eaa5033fd15897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912251"
---
# <a name="embedded-strings"></a>Stringhe incorporate

Le strutture di informazioni non conterranno stringhe incorporate. Ciò migliora l'allineamento delle strutture di informazioni e consente la flessibilità OEM nelle funzioni principali.

Qualsiasi campo di informazioni restituito in una chiamata di enumerazione che può essere successivamente usato come chiave per la chiamata a una funzione di gestione di rete GetInfo è sempre presente nel buffer di enumerazione. Se la stringa di informazioni a lunghezza variabile che specifica il valore del campo chiave non rientra, non viene restituita l'intera struttura a lunghezza fissa per la voce. Altri campi a lunghezza variabile verranno restituiti come **puntatore NULL** per il caso in cui la stringa non rientra.

 

 




