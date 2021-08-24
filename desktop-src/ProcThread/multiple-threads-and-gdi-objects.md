---
description: Per migliorare le prestazioni, l'accesso agli oggetti GDI (Graphics Device Interface), ad esempio tavolozze, contesti di dispositivo, aree e simili, non viene serializzato.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Più thread e oggetti GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a17c7edcf32341eb9b1eaff3546fbe7be219b5f924a85d4a1db1d584a0a5922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032331"
---
# <a name="multiple-threads-and-gdi-objects"></a>Più thread e oggetti GDI

Per migliorare le prestazioni, l'accesso agli oggetti GDI (Graphics Device Interface), ad esempio tavolozze, contesti di dispositivo, aree e simili, non viene serializzato. Ciò crea un potenziale rischio per i processi con più thread che condividono questi oggetti. Ad esempio, se un thread elimina un oggetto GDI mentre lo usa un altro thread, i risultati sono imprevedibili. Questo rischio può essere evitato semplicemente non condividendo oggetti GDI. Se la condivisione è inevitabile (o auspicabile), l'applicazione deve fornire i propri meccanismi per la sincronizzazione dell'accesso. Per altre informazioni sulla sincronizzazione dell'accesso, vedere [Sincronizzazione dell'esecuzione di più thread.](synchronizing-execution-of-multiple-threads.md)

 

 



