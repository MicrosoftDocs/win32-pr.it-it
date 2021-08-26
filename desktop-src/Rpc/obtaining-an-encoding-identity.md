---
title: Recupero di un'identità di codifica
description: Un'applicazione che decodifica dati codificati può ottenere l'identità della routine utilizzata per codificare i dati, prima di chiamare una routine per decodificare i dati. La routine MesInqProcEncodingId fornisce questa identità.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- RPC Remote Procedure Call , attività, recupero dell'identità di codifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a0883a1a032a76f13cfeeb6c5d6a8923146b7ee9e8184d37d5994fb5e328bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019448"
---
# <a name="obtaining-an-encoding-identity"></a>Recupero di un'identità di codifica

Un'applicazione che decodifica dati codificati può ottenere l'identità della routine utilizzata per codificare i dati, prima di chiamare una routine per decodificare i dati. La routine [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) fornisce questa identità.

A ogni routine in un'interfaccia viene  assegnato un numero di identificazione intero, denominato identificatore di routine o *ID procedura,* dal compilatore MIDL. La numerazione inizia con zero. Le librerie di runtime RPC non sono coinvolte nella conversione dell'ID procedura in una chiamata di procedura effettiva. Dato un ID procedura, l'applicazione deve fornire un modo per chiamare la procedura corretta. In genere, gli sviluppatori di applicazioni usano una serie di istruzioni **if** o (quando si usa C/C++) un'istruzione **switch** a questo scopo.

 

 




