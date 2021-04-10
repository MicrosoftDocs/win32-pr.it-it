---
title: Attributi ACF di gestione della memoria
description: Gli attributi elencati nella tabella seguente consentono di eseguire la gestione della memoria dal lato client.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- MIDL, attributi, gestione della memoria di ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12a0ee6d11a2b10e1c0fad7cd1a42411670b508
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963028"
---
# <a name="memory-management-acf-attributes"></a>Attributi ACF di gestione della memoria

Gli attributi elencati nella tabella seguente consentono di eseguire la gestione della memoria dal lato client.



| Attributo                                   | Utilizzo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**allocare**](allocate.md)                | Specifica il modo in cui l'applicazione client e lo stub allocano e rilasciano memoria per i puntatori. Questo attributo è particolarmente utile quando si desidera che determinate strutture del puntatore rimangano accessibili all'applicazione server dopo che la chiamata RPC viene restituita al client. È anche possibile usare l'attributo [**allocate**](allocate.md) per indirizzare lo stub per calcolare le dimensioni di tutta la memoria a cui viene fatto riferimento tramite il puntatore del tipo specificato e per eseguire una singola chiamata all' [**\_ utente MIDL \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function). |
| [**\_conteggio byte**](byte-count.md)           | Consente di creare un blocco di memoria persistente e contiguo che può essere riutilizzato in più chiamate di procedure remote. In questo modo l'applicazione client evita l'overhead di allocare e rilasciare ripetutamente memoria che può includere più puntatori e altre strutture di dati complesse.                                                                                                                                                                                                                                                      |
| [**Abilita \_ allocazione**](enable-allocate.md) | Specifica che il codice stub del server deve abilitare l'ambiente di gestione della memoria stub.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 