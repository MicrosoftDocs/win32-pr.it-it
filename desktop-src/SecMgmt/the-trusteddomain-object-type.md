---
description: I sistemi basati su Windows possono avere più istanze del tipo di oggetto TrustedDomain.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: Tipo di oggetto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0a4e6eca0790d877a9a23e4d83725d4e80798
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750858"
---
# <a name="the-trusteddomain-object-type"></a>Tipo di oggetto TrustedDomain

I sistemi basati su Windows possono avere più istanze del tipo di oggetto [**trustedDomain**](trusteddomain-object.md) . Gli oggetti **trustedDomain** hanno due campi che devono essere univoci tra tutti gli oggetti **trustedDomain** :

-   Nome del [ **trustedDomain**](trusteddomain-object.md)
-   [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) di [**trustedDomain**](trusteddomain-object.md).

Il tentativo di creare un nuovo oggetto **trustedDomain** con un nome o un SID già in uso da un altro oggetto **trustedDomain** verrà rifiutato.

 

 
