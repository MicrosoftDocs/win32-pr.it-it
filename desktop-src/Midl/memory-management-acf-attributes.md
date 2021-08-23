---
title: Attributi ACF di Gestione memoria
description: Gli attributi elencati nella tabella seguente consentono di eseguire la gestione della memoria dal lato client.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- ACF MIDL , attributi, gestione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d7df6f020d8531f0c1ca8bebdd6bf59270f2ed22c821e2c183c9da6936e306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013749"
---
# <a name="memory-management-acf-attributes"></a>Attributi ACF di Gestione memoria

Gli attributi elencati nella tabella seguente consentono di eseguire la gestione della memoria dal lato client.



| Attributo                                   | Utilizzo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Allocare**](allocate.md)                | Specifica il modo in cui l'applicazione client e lo stub allocano e rilasciano memoria per i puntatori. Questo attributo è particolarmente utile quando si vuole che determinate strutture puntatore rimangano accessibili all'applicazione server dopo il ritorno della chiamata di procedura remota al client. È anche possibile usare l'attributo [**allocate**](allocate.md) per indirizzare lo stub per calcolare le dimensioni di tutta la memoria a cui si fa riferimento tramite il puntatore del tipo specificato ed eseguire una singola chiamata a [**midl \_ user \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function). |
| [**numero di \_ byte**](byte-count.md)           | Consente di creare un blocco di memoria persistente e contiguo che può essere riutilizzato su più chiamate di procedura remota. In questo modo l'applicazione client viene liberata dall'overhead dovuto all'allocazione e al rilascio ripetuti di memoria che può includere più puntatori e altre strutture di dati complesse.                                                                                                                                                                                                                                                      |
| [**abilitare \_ l'allocazione**](enable-allocate.md) | Specifica che il codice stub del server deve abilitare l'ambiente di gestione della memoria stub.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 