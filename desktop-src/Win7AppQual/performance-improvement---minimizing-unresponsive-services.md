---
description: Procedure consigliate per ridurre al minimo i servizi che non rispondono
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Procedure consigliate per ridurre al minimo i servizi che non rispondono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90416e8256383e16fd78c436dfaa8d6a2186c540
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087999"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a>Procedure consigliate per ridurre al minimo i servizi che non rispondono

## <a name="affected-platform"></a>Piattaforma interessata

 **Client** : Windows Vista \| Windows 7  

## <a name="description"></a>Descrizione

I servizi che non rispondono possono comportare timeout, sessioni terminate e persino perdita di dati. L'utilizzo di procedure consigliate può ridurre notevolmente il numero di servizi che non rispondono.

## <a name="best-practices"></a>Procedure consigliate

Assicurarsi che le applicazioni e tutti i relativi servizi e driver dipendenti rispondano alle notifiche relative all'alimentazione e all'arresto del sistema.

-   Tutte le applicazioni devono rispondere tempestivamente e in modo appropriato ai messaggi di arresto, ad esempio WM QUERYENDSESSION e WM ENDSESSION che indicano che è in corso \_ \_ un arresto.
-   Tutti i servizi devono rispondere tempestivamente alle notifiche di arresto di Gestione controllo servizi. In caso contrario, il computer li considera come non risponde e avvia un timeout di 20 secondi e li arresta, aprendo la possibilità di perdere i dati. Ciò aggiunge anche 20 secondi all'ora di arresto di un computer.
-   Tutti i servizi con dipendenze del driver di dispositivo kernel devono rispondere tempestivamente e in modo appropriato alla notifica \_ IRP MJ SHUTDOWN nelle \_ routine DispatchShutdown.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

<dl>

[Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



