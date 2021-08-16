---
description: Windows sistemi basati su certificati possono avere più istanze del tipo di oggetto TrustedDomain.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: Tipo di oggetto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab860f9192e48433242251578a20a45bf294164c0bffff8b6f00562a1442e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004839"
---
# <a name="the-trusteddomain-object-type"></a>Tipo di oggetto TrustedDomain

Windows sistemi basati su certificati possono avere più istanze del [**tipo di oggetto TrustedDomain.**](trusteddomain-object.md) **Gli oggetti TrustedDomain** hanno due campi che devono essere univoci tra tutti **gli oggetti TrustedDomain:**

-   Nome dell'oggetto [ **TrustedDomain**](trusteddomain-object.md)
-   Identificatore [*di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) di [**TrustedDomain.**](trusteddomain-object.md)

Il tentativo di creare un nuovo oggetto **TrustedDomain** con un nome o un SID già in uso da un altro oggetto **TrustedDomain** verrà rifiutato.

 

 
