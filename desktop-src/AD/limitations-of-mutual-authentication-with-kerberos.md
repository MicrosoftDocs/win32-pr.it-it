---
title: Limitazioni dell'autenticazione reciproca con Kerberos
description: Sia l'account del client che l'account del servizio devono essere in domini Windows 2000 nativi o in modalità mista perché i servizi Kerberos non sono disponibili nei domini di livello inferiore.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77bdc2f8cfe87d3cece32987ee0958000b1186775257013ce27f5950c6ac8f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187065"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a>Limitazioni dell'autenticazione reciproca con Kerberos

Sia l'account del client che l'account del servizio devono essere in domini Windows 2000 nativi o in modalità mista perché i servizi Kerberos non sono disponibili nei domini di livello inferiore. Inoltre, gli account client e di servizio devono essere nella stessa foresta perché il KDC del client usa il catalogo globale per cercare il nome dell'entità servizio.

Sia il servizio che il client devono essere in esecuzione in Windows 2000. In caso contrario, l'autenticazione reciproca con Kerberos avrà esito negativo perché le versioni precedenti di Windows non supportano Kerberos.

I nomi delle entità servizio devono includere il nome DNS del server host in cui è in esecuzione il servizio. È necessario usare il nome DNS.

 

 




