---
title: Ripristino e riavvio di un'applicazione
description: Scrivere programmi di installazione personalizzati per riavviare automaticamente un'applicazione che è stata arrestata per completare un aggiornamento. Salvare i dati e configurare il ripristino dell'applicazione prima di chiudere i programmi.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- affidabilità
- affidabilità software
- ripristino dell'applicazione
- riavvio dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862236fad876307b0662a8444775c78673b92983
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856802"
---
# <a name="application-recovery-and-restart"></a>Ripristino e riavvio di un'applicazione

## <a name="purpose"></a>Scopo

Un'applicazione può usare il ripristino e il riavvio dell'applicazione (ARR) per salvare i dati e le informazioni sullo stato prima che l'applicazione venga chiusa a causa di un'eccezione non gestita o quando l'applicazione smette di rispondere. Se richiesto, viene riavviata anche l'applicazione.

Un'applicazione può essere riavviata anche se un programma di installazione aggiorna un componente dell'applicazione o se il computer deve essere riavviato come risultato di un aggiornamento. Si noti che per supportare il riavvio automatico dell'applicazione dopo l'aggiornamento di un'applicazione da parte di un programma di installazione, è necessario creare l'applicazione e il programma di installazione in modo appropriato. Per informazioni dettagliate, vedere [la pagina relativa alla registrazione per il riavvio dell'applicazione](registering-for-application-restart.md).

## <a name="developer-audience"></a>Sviluppatori

ARR è progettato per gli sviluppatori C e C++.

## <a name="run-time-requirements"></a>Requisiti di runtime

ARR è disponibile a partire dal sistema operativo Windows Vista.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                   | Descrizione                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Utilizzo del ripristino dell'applicazione e riavvio](using-application-recovery-and-restart.md)<br/>         | Guida procedurale per la registrazione per il ripristino e il riavvio.<br/> |
| [Riferimento al ripristino e al riavvio dell'applicazione](application-recovery-and-restart-reference.md)<br/> | Informazioni di riferimento per l'API ARR. <br/>                    |



 

 

 





