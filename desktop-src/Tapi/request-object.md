---
description: L'oggetto richiesta viene creato usando COM CoCreateInstance ed espone un'interfaccia, ITRequest.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Oggetto Request
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcf6da101c3642ffe31b05efb18279a79bcfc28ed24af7a959f3275d9cbc4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905891"
---
# <a name="request-object"></a>Oggetto Request

L'oggetto richiesta viene creato usando **COM CoCreateInstance** ed espone un'interfaccia, [**ITRequest.**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest) Questa interfaccia espone il metodo [**MakeCall,**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) che consente a un'applicazione TAPI 3 di usare la telefonia assistita. La telefonia assistita offre alle applicazioni abilitate per la telefonia un meccanismo semplice per effettuare chiamate telefoniche senza richiedere allo sviluppatore di diventare completamente intesi nella telefonia.

Ad esempio, un'applicazione foglio di calcolo può aggiungere un pulsante "Effettua chiamata" usando telefonia assistita senza implementare i controlli più elaborati disponibili in un'applicazione TAPI completa.

Per altre [informazioni, vedere Cenni preliminari sulla](assisted-telephony-overview.md) telefonia assistita.

 

 



