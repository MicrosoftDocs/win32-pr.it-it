---
description: Procedure consigliate per ridurre al minimo i servizi che non rispondono
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Procedure consigliate per ridurre al minimo i servizi che non rispondono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3f37620fc00834b3c25a92292c889785818c2810cac7c12e788de8bf1fb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994851"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a>Procedure consigliate per ridurre al minimo i servizi che non rispondono

## <a name="affected-platform"></a>Piattaforma interessata

 **Client** : Windows Vista \| Windows 7  

## <a name="description"></a>Descrizione

I servizi che non rispondono possono causare timeout, sessioni terminate e persino perdita di dati. L'utilizzo di procedure consigliate può ridurre notevolmente l'occorrenza di servizi che non rispondono.

## <a name="best-practices"></a>Procedure consigliate

Assicurarsi che le applicazioni e tutti i relativi driver e servizi dipendenti rispondano alle notifiche relative all'alimentazione e all'arresto del sistema.

-   Tutte le applicazioni devono rispondere tempestivamente e in modo appropriato ai messaggi di arresto, ad esempio WM QUERYENDSESSION e WM ENDSESSION che indicano che è \_ \_ in corso un arresto.
-   Tutti i servizi devono rispondere prontamente alle notifiche di arresto di Gestione controllo servizi. In caso contrario, il computer li considera non risponde e avvia un timeout di 20 secondi e li arresta, aprendo la possibilità di perdita di dati. Ciò aggiunge anche 20 secondi all'ora di arresto di un computer.
-   Tutti i servizi con dipendenze del driver di dispositivo del kernel devono rispondere in modo tempestivo e appropriato alla notifica DI ARRESTO MJ IRP nelle \_ \_ routine DispatchShutdown.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

<dl>

[Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



