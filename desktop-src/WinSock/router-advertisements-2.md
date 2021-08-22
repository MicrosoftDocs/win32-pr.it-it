---
description: Il contenuto degli annunci del router IPv6 viene derivato automaticamente dalle route pubblicate nella tabella di routing. Le route non pubblicate vengono usate per il routing, ma vengono ignorate durante la creazione di annunci router.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: Annunci router IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef8a7be2139c03d94e8a84eae410e9f4f2e92da6059def1ef89997138009d351
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612941"
---
# <a name="ipv6-router-advertisements"></a>Annunci router IPv6

Il contenuto degli annunci del router IPv6 viene derivato automaticamente dalle route pubblicate nella tabella di routing. Le route non pubblicate vengono usate per il routing, ma vengono ignorate durante la creazione di annunci router.

Gli annunci router per IPv6 contengono sempre un'opzione di indirizzo del livello di collegamento di origine e un'opzione MTU. Il valore dell'opzione MTU è tratto dall'MTU del collegamento corrente dell'interfaccia mittente. Questo valore può essere modificato con il comando ipv6 ifc mtu.

L'annuncio router ha una durata del router diversa da zero solo se è presente una route predefinita pubblicata. Una route predefinita è una route per il prefisso di lunghezza zero.

Le route on-link pubblicate comportano opzioni di informazioni sul prefisso negli annunci del router. Se il prefisso on-link ha 64 bit, l'opzione delle informazioni sul prefisso ha entrambi i bit L e A impostati e gli host che lo ricevono configurano automaticamente gli indirizzi.

Un'interfaccia che invia annunci router configura automaticamente anche gli indirizzi in base alle opzioni relative alle informazioni sul prefisso che invia.

È consigliabile una durata non media finita su tutte le route pubblicate (ad esempio, 30 minuti). Se si decide di ritirare una route, è possibile modificare la route in modo che abbia una durata obsoleta. La route avrà validità nel corso di diversi annunci router e quindi scompare sia dal router che da tutti gli host che ricevono gli annunci del router.

Le route individuate dagli host tramite annunci router hanno un'età e non vengono pubblicate. Indirizzi configurati automaticamente anche dall'età degli annunci del router.

 

 



