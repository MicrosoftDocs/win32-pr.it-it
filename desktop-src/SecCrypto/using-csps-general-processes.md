---
description: Quando si usano i provider del servizio di crittografia CSP, tenere presenti le convenzioni seguenti.
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 'Uso dei CSP: processi generali'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308635"
---
# <a name="using-csps-general-processes"></a>Uso dei CSP: processi generali

Quando si usano i [*provider del servizio di crittografia*](../secgloss/c-gly.md) CSP, tenere presenti le convenzioni seguenti.

## <a name="private-key-caching"></a>Caching della chiave privata

Un CSP può memorizzare nella cache alcune [*chiavi private*](../secgloss/p-gly.md). È possibile controllare la memorizzazione nella cache della chiave privata in un livello globale, ma non in base all'applicazione. Le modifiche di Caching vengono apportate modificando determinate impostazioni del registro di sistema. Per altre informazioni, vedere [**costanti di caching della chiave privata**](private-key-caching-constants.md).

## <a name="example-code-conventions"></a>Convenzioni del codice di esempio

Per fornire codice più conciso e leggibile, alcuni principi di buone procedure di programmazione non sono sempre seguiti negli esempi. In particolare:

-   Vengono visualizzate solo le risposte di errore limitate. I programmi ben scritti e completi controllano i codici di errore restituiti ed eseguono le azioni appropriate quando viene rilevato un errore.
-   Viene eseguita solo la memoria limitata e la gestione delle risorse. Programmi ben scritti e completi eliminano tutte le chiavi e gli [*hash*](../secgloss/h-gly.md), liberano tutta la memoria allocata, chiudono tutti i file e rilasciano tutti gli handle. Questi esempi forniscono solo dimostrazioni limitate dell'utilizzo di funzioni che eseguono queste attività. Questi esempi non eseguono attività di memoria o di gestione delle risorse in caso di interruzione del programma a causa di errori.

Negli argomenti seguenti vengono presentate informazioni generali sugli esempi di procedure, oltre a codice di esempio.

-   [Recupero di dati di lunghezza sconosciuta](retrieving-data-of-unknown-length.md)
-   [Enumerazione dei protocolli supportati](enumerating-supported-protocols.md)

 

 
