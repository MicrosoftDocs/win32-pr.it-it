---
description: Il mapper di invio viene creato utilizzando COM CoCreateInstance ed espone un'interfaccia, ITDispatchMapper.
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: Mapper di invio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed0a3a6cbc906861f5e95694bfd75aec6f5791f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311902"
---
# <a name="dispatch-mapper"></a>Mapper di invio

Il mapper di invio viene creato utilizzando COM **CoCreateInstance** ed espone un'interfaccia, [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper). Questa interfaccia consente a un'applicazione di recuperare il puntatore di invio di un'altra interfaccia su un oggetto, dato il puntatore di invio di un'interfaccia e il GUID di un altro. Questa interfaccia viene fornita per aiutare i programmatori che utilizzano applicazioni di scripting che non consentono di eseguire immediatamente il polling delle interfacce in un oggetto.

Il mapper di invio utilizza l'interfaccia **IObjectSafety** di un oggetto per assicurarsi che l'oggetto sia sicuro per l'esecuzione di script sull'interfaccia richiesta. Se l'oggetto non implementa **IObjectSafety** o se l'oggetto non è sicuro su questa interfaccia particolare, la chiamata avrà esito negativo.

 

 



