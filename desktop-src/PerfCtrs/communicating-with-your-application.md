---
description: In genere, un provider fornisce dati per conto di un'applicazione.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Comunicazione con l'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6def58d3e03676f3b1b46ba3ebd756eb3adc6196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881774"
---
# <a name="communicating-with-your-application"></a>Comunicazione con l'applicazione

In genere, un provider fornisce dati per conto di un'applicazione. Ad esempio, un server potrebbe creare una DLL di prestazioni per fornire i dati del contatore. La comunicazione tra un'applicazione e il relativo provider differisce per le applicazioni in modalità utente e kernel. I provider vengono eseguiti in modalità utente. Per questo motivo, le applicazioni in modalità utente, ad esempio le applicazioni di stampa e visualizzazione, possono utilizzare qualsiasi tecnica per la comunicazione interprocesso, ad esempio le named pipe, il mapping dei file o la RPC. Tuttavia, le applicazioni in modalità kernel devono fornire un'interfaccia IOCTL che restituisca i dati sulle prestazioni al provider.

> [!WARNING]
> Non usare COM come meccanismo IPC. Il sistema non è in grado di garantire lo stato di inizializzazione COM del thread che chiama l'interfaccia. Pertanto, la DLL potrebbe non essere in grado di inizializzare COM e raccogliere i dati.

 

 

 



