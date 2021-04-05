---
title: Ottenere un'identità di codifica
description: Un'applicazione che decodifica i dati codificati può ottenere l'identità della routine utilizzata per codificare i dati, prima di chiamare una routine per decodificarla. La routine MesInqProcEncodingId fornisce questa identità.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- RPC (Remote Procedure Call), attività, acquisizione dell'identità di codifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8591e030913d659fb48034e4c386295773227f7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713072"
---
# <a name="obtaining-an-encoding-identity"></a>Ottenere un'identità di codifica

Un'applicazione che decodifica i dati codificati può ottenere l'identità della routine utilizzata per codificare i dati, prima di chiamare una routine per decodificarla. La routine [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) fornisce questa identità.

A ogni procedura di un'interfaccia viene assegnato un numero di identificazione intero, detto *identificatore di routine* o *ID proc*, dal compilatore MIDL. La numerazione inizia con zero. Le librerie di runtime RPC non sono necessarie per tradurre l'ID procedura in una chiamata di procedura effettiva. Dato un ID proc, l'applicazione deve fornire un metodo per chiamare la procedura corretta. In genere, gli sviluppatori di applicazioni utilizzano una serie di istruzioni **if** oppure, quando si utilizza C/C++, un'istruzione **Switch** a questo scopo.

 

 




