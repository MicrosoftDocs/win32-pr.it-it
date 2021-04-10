---
description: .
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Procedure consigliate per ridurre al minimo i servizi che non rispondono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e1fbad7fe60c4165ebb97847c303482314f68e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885238"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a>Procedure consigliate per ridurre al minimo i servizi che non rispondono

## <a name="affected-platform"></a>Piattaforma interessata

 **Client** – Windows Vista \| Windows 7  

## <a name="description"></a>Descrizione

I servizi che non rispondono possono causare timeout, sessioni interrotte e persino dati persi. L'utilizzo delle procedure consigliate può ridurre notevolmente l'occorrenza di servizi che non rispondono.

## <a name="best-practices"></a>Procedure consigliate

Assicurarsi che le applicazioni e tutti i relativi servizi e driver dipendenti rispondano alle notifiche di accensione e spegnimento del sistema.

-   Tutte le applicazioni devono rispondere tempestivamente e in modo appropriato ai messaggi di chiusura, ad esempio WM \_ QUERYENDSESSION e WM \_ ENDSESSION, che indicano che è in corso l'arresto.
-   Tutti i servizi devono rispondere tempestivamente alle notifiche di chiusura di SCM. In caso contrario, il computer li considera non risponde e avvia un timeout di 20 secondi e li arresta, aprendo la possibilità di perdita di dati. Vengono inoltre aggiunti 20 secondi all'ora di arresto dell'arresto di un computer.
-   Tutti i servizi che hanno dipendenze del driver di dispositivo kernel devono rispondere tempestivamente e in modo appropriato alla \_ notifica di arresto per l'IRP \_ di MJ nelle routine DispatchShutdown.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

<dl>

[Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



