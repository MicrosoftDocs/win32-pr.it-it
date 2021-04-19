---
description: L'oggetto Request viene creato utilizzando COM CoCreateInstance ed espone un'interfaccia, ITRequest.
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Oggetto Request
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51e81cae01f2624ba863b304c0a5f732b221199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311878"
---
# <a name="request-object"></a>Oggetto Request

L'oggetto Request viene creato utilizzando COM **CoCreateInstance** ed espone un'interfaccia, [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest). Questa interfaccia espone il metodo [**MakeCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) , che consente a un'applicazione TAPI 3 di utilizzare la telefonia assistita. La telefonia assistita offre applicazioni abilitate per la telefonia con un semplice meccanismo per effettuare chiamate telefoniche senza che lo sviluppatore debba essere completamente alfabetizzato nella telefonia.

Ad esempio, un'applicazione per fogli di calcolo può aggiungere un pulsante "make Call" utilizzando la telefonia assistita senza implementare i controlli più elaborati disponibili in un'applicazione TAPI completa.

Per ulteriori informazioni, vedere la [Panoramica della telefonia assistita](assisted-telephony-overview.md) .

 

 



