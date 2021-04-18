---
description: Il contenuto degli annunci router IPv6 viene derivato automaticamente dalle route pubblicate nella tabella di routing. Le route non pubblicate vengono utilizzate per il routing, ma vengono ignorate durante la creazione di annunci router.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: Annunci router IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a75b31a988595cba85d23dbafc1bd93ffff4ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310441"
---
# <a name="ipv6-router-advertisements"></a>Annunci router IPv6

Il contenuto degli annunci router IPv6 viene derivato automaticamente dalle route pubblicate nella tabella di routing. Le route non pubblicate vengono utilizzate per il routing, ma vengono ignorate durante la creazione di annunci router.

Gli annunci router per IPv6 contengono sempre un'opzione relativa all'indirizzo del livello di collegamento di origine e un'opzione MTU. Il valore dell'opzione MTU viene tratto dall'MTU del collegamento corrente dell'interfaccia mittente. Questo valore può essere modificato con il comando IPv6 IFC.

L'annuncio router ha una durata di un router diverso da zero se è presente una route predefinita pubblicata. Una route predefinita è una route per il prefisso di lunghezza zero.

Le route di collegamento pubblicate generano le opzioni relative alle informazioni sul prefisso negli annunci router. Se il prefisso on-link ha 64 bit, l'opzione relativa alle informazioni sul prefisso include sia il set di bit che gli host che lo ricevono. gli indirizzi vengono configurati automaticamente.

Un'interfaccia che invia annunci router consente anche di configurare automaticamente gli indirizzi in base alle opzioni di informazioni sul prefisso che invia.

Si consiglia di usare una durata di non invecchiamento finita in tutte le route pubblicate, ad esempio 30 minuti. Se si decide di ritirare una route, è possibile modificare la route in modo che abbia una durata di invecchiamento. La route sarà di età nel corso di diversi annunci router e quindi scomparirà sia dal router che dagli host che ricevono gli annunci del router.

Le route che gli host trovano tramite gli annunci router Age e non vengono pubblicate. Indirizzi configurati automaticamente dall'età degli annunci router.

 

 



