---
title: Lunghezze del buffer delle funzioni di gestione di rete
description: Questo argomento illustra i requisiti per le lunghezze del buffer delle funzioni se usato con le API di gestione della rete.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858b01de7b0b4cecb9eaea9f93bb541cb95fe9b394e74616427910abe3b33403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911741"
---
# <a name="network-management-function-buffer-lengths"></a>Lunghezze del buffer delle funzioni di gestione di rete

Questo argomento illustra i requisiti per le lunghezze del buffer delle funzioni se usato con le API di gestione della rete.

Le applicazioni che specificano le dimensioni del buffer quando chiamano funzioni di enumerazione di gestione di rete (e varie funzioni di recupero dati) devono specificare buffer sufficientemente grandi da contenere la struttura o le strutture di informazioni restituite più le stringhe a cui puntano i relativi membri. Se non si specifica un buffer sufficientemente grande per ricevere tutte le voci disponibili, la funzione restituisce ERROR \_ MORE \_ DATA. Le chiamate di enumerazione non restituiscono voci parziali.

Alcune funzioni di gestione di rete accettano un parametro advisory maximum data-length, *prefmaxlen*. Questo parametro consente a un'applicazione di suggerire il numero di byte che il server deve restituire da una chiamata di funzione.

Se si specifica il valore MAX PREFERRED LENGTH nel \_ \_ parametro *prefmaxlen,* le funzioni di gestione della rete allocano la quantità di memoria necessaria per i dati.

Per altre informazioni, vedere [Buffer delle funzioni di gestione di rete](network-management-function-buffers.md).

 

 




