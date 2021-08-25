---
title: Implementazione Active Accessibility nativa
description: Gli elementi dell'interfaccia utente che implementano l'interfaccia IAccessible forniscono un'implementazione nativa.
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4414fa1cd40b66b0971d7c74f484b90c62f86db64722abaabc0e8eea60b14fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859931"
---
# <a name="native-active-accessibility-implementation"></a>Implementazione Active Accessibility nativa

Gli elementi dell'interfaccia utente che implementano [**l'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) forniscono *un'implementazione nativa.* Anche se il costo di sviluppo per l'implementazione di **IAccessible** (o qualsiasi altra interfaccia Component Object Model (COM) può essere elevato, il vantaggio è il controllo completo sulle informazioni esposte ai client.

Se l'applicazione usa controlli personalizzati o altri controlli che non possono essere proxy da Oleacc.dll, è necessario fornire un'implementazione nativa.

 

 




