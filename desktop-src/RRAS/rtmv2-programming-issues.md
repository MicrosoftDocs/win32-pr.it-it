---
title: Problemi di programmazione RTMv2
description: Le funzioni RTMv2 vengono scritte con i presupposti seguenti.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Problemi di programmazione, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584568fc3c4e7a46a2a2114781b81465d893b80978471aa3149d93d38f0c8c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035591"
---
# <a name="rtmv2-programming-issues"></a>Problemi di programmazione RTMv2

Le funzioni RTMv2 vengono scritte con i presupposti seguenti.

-   Le funzioni RTMv2 non allocano memoria per il client. Il client deve sempre allocare memoria.
-   Quando un client annulla la registrazione, deve eseguire operazioni di pulizia, ad esempio il rilascio di tutta la memoria allocata.
-   I client devono rilasciare correttamente gli handle. Possono verificarsi perdite di memoria se un client non osserva questa procedura.

 

 




