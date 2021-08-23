---
description: In genere, un provider fornisce dati per conto di un'applicazione.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Comunicazione con l'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb696c0c12ed8de542b07067fe16e13c9c098cb712393975e82d948bc3238979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061229"
---
# <a name="communicating-with-your-application"></a>Comunicazione con l'applicazione

In genere, un provider fornisce dati per conto di un'applicazione. Ad esempio, un server potrebbe creare una DLL delle prestazioni per fornire i dati dei contatori. La comunicazione tra un'applicazione e il relativo provider è diversa per le applicazioni in modalità utente e kernel. I provider vengono eseguiti in modalità utente. Per questo scopo, le applicazioni in modalità utente, ad esempio le applicazioni di stampa e visualizzazione, possono usare qualsiasi tecnica per la comunicazione interprocesso, ad esempio named pipe, mapping di file o RPC. Tuttavia, le applicazioni in modalità kernel devono fornire un'interfaccia IOCTL che restituisce i dati sulle prestazioni al provider.

> [!WARNING]
> Non usare COM come meccanismo IPC. Il sistema non può garantire lo stato di inizializzazione COM del thread che chiama l'interfaccia . Pertanto, la DLL potrebbe non essere in grado di inizializzare correttamente COM e raccogliere i dati.

 

 

 



