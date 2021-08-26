---
title: Ripristino e riavvio di un'applicazione
description: Scrivere programmi di installazione personalizzati per riavviare automaticamente un'applicazione arrestata per completare un aggiornamento. Salvare i dati e configurare il ripristino dell'applicazione prima di uscire dal programma.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- affidabilità
- affidabilità del software
- ripristino di applicazioni
- riavvio dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31d6c8ef342b9e1781297d547358317a90d515002e6ef3e529b8d7a0c50aa09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024601"
---
# <a name="application-recovery-and-restart"></a>Ripristino e riavvio di un'applicazione

## <a name="purpose"></a>Scopo

Un'applicazione può usare Application Recovery and Restart (ARR) per salvare i dati e le informazioni sullo stato prima che l'applicazione venga chiusa a causa di un'eccezione non gestita o quando l'applicazione smette di rispondere. Anche l'applicazione viene riavviata, se richiesto.

Un'applicazione può essere riavviata anche se un programma di installazione aggiorna un componente dell'applicazione o se il computer deve essere riavviato come risultato di un aggiornamento. Si noti che per supportare il riavvio automatico dell'applicazione dopo l'aggiornamento di un'applicazione da parte di un programma di installazione, è necessario creare sia l'applicazione che il programma di installazione in modo appropriato. Per informazioni dettagliate, vedere [Registrazione per il riavvio dell'applicazione](registering-for-application-restart.md).

## <a name="developer-audience"></a>Sviluppatori

ARR è progettato per gli sviluppatori C e C++.

## <a name="run-time-requirements"></a>Requisiti di runtime

ARR è disponibile a partire dal sistema operativo Windows Vista.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                   | Descrizione                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Uso del ripristino e del riavvio dell'applicazione](using-application-recovery-and-restart.md)<br/>         | Guida procedurale per la registrazione per il ripristino e il riavvio.<br/> |
| [Informazioni di riferimento su Ripristino applicazioni e riavvio](application-recovery-and-restart-reference.md)<br/> | Informazioni di riferimento per l'API ARR. <br/>                    |



 

 

 





