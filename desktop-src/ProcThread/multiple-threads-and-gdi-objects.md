---
description: Per migliorare le prestazioni, non è possibile serializzare l'accesso a oggetti GDI (Graphics Device Interface), ad esempio tavolozze, contesti di dispositivo, aree e così come.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Più thread e oggetti GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5822539248be5189f7a8e7fb15f4ef8a42ff1b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311983"
---
# <a name="multiple-threads-and-gdi-objects"></a>Più thread e oggetti GDI

Per migliorare le prestazioni, non è possibile serializzare l'accesso a oggetti GDI (Graphics Device Interface), ad esempio tavolozze, contesti di dispositivo, aree e così come. Ciò crea un rischio potenziale per i processi con più thread che condividono questi oggetti. Se, ad esempio, un thread elimina un oggetto GDI mentre viene utilizzato da un altro thread, i risultati sono imprevedibili. Questo pericolo può essere evitato semplicemente non condividendo oggetti GDI. Se la condivisione è inevitabile (o auspicabile), l'applicazione deve fornire i propri meccanismi per la sincronizzazione dell'accesso. Per ulteriori informazioni sulla sincronizzazione dell'accesso, vedere [sincronizzazione dell'esecuzione di più thread](synchronizing-execution-of-multiple-threads.md).

 

 



