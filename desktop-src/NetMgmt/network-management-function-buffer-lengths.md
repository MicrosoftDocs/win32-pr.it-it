---
title: Lunghezze del buffer della funzione di gestione di rete
description: Questo argomento illustra i requisiti per le lunghezze del buffer di funzione quando viene usato con le API di gestione di rete.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5003f739d235a099adb9f4f403c15c67bd9169e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856233"
---
# <a name="network-management-function-buffer-lengths"></a>Lunghezze del buffer della funzione di gestione di rete

Questo argomento illustra i requisiti per le lunghezze del buffer di funzione quando viene usato con le API di gestione di rete.

Le applicazioni che specificano le dimensioni del buffer durante la chiamata di funzioni di enumerazione di gestione della rete (e varie funzioni di recupero dei dati) devono specificare buffer sufficientemente grandi da conservare la struttura o le strutture di informazioni restituite più le stringhe a cui puntano i membri. Se non si specifica un buffer sufficientemente grande per ricevere tutte le voci disponibili, la funzione restituisce l'errore di \_ altri \_ dati. Le chiamate di enumerazione non restituiscono voci parziali.

Alcune funzioni di gestione di rete accettano un parametro di lunghezza massima dei dati consultivo, *prefMaxLen*. Questo parametro consente a un'applicazione di suggerire il numero di byte che il server deve restituire da una chiamata di funzione.

Se si specifica la lunghezza massima \_ preferita del valore \_ nel parametro *prefMaxLen* , le funzioni di gestione della rete allocano la quantità di memoria necessaria per i dati.

Per ulteriori informazioni, vedere [buffer di funzioni di gestione di rete](network-management-function-buffers.md).

 

 




