---
description: L'indirizzamento locale del collegamento IPv6 nei messaggi SOAP rappresenta una sfida univoca, perché gli indirizzi locali del collegamento IPv6 richiedono un ID di ambito significativo, ma l'ID ambito ha un significato solo per il computer locale.
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: Uso di indirizzi locali di collegamento IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c1719e4e6d374e7afd859b80cd1bc14c4c841cb7dceee149f14d0acb777f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897161"
---
# <a name="using-ipv6-link-local-addresses"></a>Uso di indirizzi locali di collegamento IPv6

L'indirizzamento locale del collegamento IPv6 nei messaggi SOAP rappresenta una sfida univoca, perché gli indirizzi locali del collegamento IPv6 richiedono un ID di ambito significativo, ma l'ID ambito ha un significato solo per il computer locale. Tutte le implementazioni client e dispositivo devono rimuovere l'ID ambito prima di inviare un indirizzo locale del collegamento IPv6 in un messaggio SOAP. Inoltre, quando un indirizzo locale del collegamento IPv6 viene ricevuto in un messaggio, l'interfaccia su cui è stato ricevuto il messaggio deve essere nota in modo che sia possibile ricostruire l'indirizzo locale del collegamento completo con ID ambito.

 

 



