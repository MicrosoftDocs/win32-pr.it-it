---
title: Caricamento di un carattere
description: Caricamento di un carattere
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78d796df5c1699b405e8cae1dbae0e7d7d8d37932aa50534fa7331a458dc54a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748404"
---
# <a name="loading-a-character"></a>Caricamento di un carattere

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per animare un carattere, è prima necessario caricare il carattere. Usare il [**metodo Load**](load-method.md) per caricare i dati del carattere. Microsoft Agent supporta due formati per i dati di animazione e di carattere: un singolo file strutturato e file separati. In genere, si usa il formato di file singolo (. ACS) quando i dati vengono archiviati in locale. Formato a più file (. Acf. ACA) funziona meglio quando si vogliono scaricare le animazioni singolarmente, ad esempio quando si accede alle animazioni da un server HTTP.

Un'applicazione client può caricare una sola istanza dello stesso carattere. Qualsiasi tentativo di caricare lo stesso carattere più volte avrà esito negativo. Tuttavia, un'applicazione può avere più istanze dello stesso carattere caricate fornendo connessioni separate a Microsoft Agent. Ad esempio, un'applicazione potrebbe caricare lo stesso carattere da due copie del controllo Microsoft Agent.

È anche possibile definire caratteri personalizzati da usare con Microsoft Agent. È possibile usare qualsiasi strumento di rendering preferito per creare le immagini, purché si ostino file Windows in formato bitmap. Per assemblare e compilare le immagini di un carattere in animazioni da usare con Microsoft Agent, usare Microsoft Agent Character Editor. Questo strumento consente di definire le proprietà predefinite di un carattere, nonché di definire animazioni per il carattere. L'Editor caratteri di Microsoft Agent consente inoltre di selezionare il formato di file appropriato quando si crea un carattere.

 

 




