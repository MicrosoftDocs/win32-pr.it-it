---
description: Il flusso di informazioni di riepilogo contiene informazioni sul pacchetto che possono essere visualizzate tramite Microsoft Windows Explorer.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: Informazioni sul flusso di informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5178edc9fe2a94ddd2812abb8161c88423cc17cd033d228b066d5ce74b9f1694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146034"
---
# <a name="about-the-summary-information-stream"></a>Informazioni sul flusso di informazioni di riepilogo

Il flusso di informazioni di riepilogo contiene informazioni sul pacchetto che possono essere visualizzate tramite Microsoft Windows Explorer. Queste informazioni sono accessibili tramite **l'interfaccia IStream.** È l'autore a fornire i valori per ognuna di queste proprietà.

Il flusso di informazioni di riepilogo usa COM per fornire l'archiviazione strutturata dei database. COM supporta il concetto di archiviazione strutturata accessibile tramite **l'interfaccia IStream.** L'archiviazione strutturata, a sua volta, supporta il concetto di set di proprietà come metodo flessibile per la serializzazione di quasi tutte le informazioni. La specifica COM definisce un singolo set di proprietà standard, informazioni di riepilogo, che viene usato per popolare le finestre delle proprietà visualizzabili da Windows Explorer. Pertanto, le informazioni archiviate nel flusso di informazioni di riepilogo possono essere visualizzate dagli utenti quando fanno clic con il pulsante destro del mouse su un database o una trasformazione del programma di installazione e [selezionano Proprietà](about-properties.md).

Per un elenco del set di proprietà di riepilogo, vedere [Summary Information Stream Property Set](summary-information-stream-property-set.md).

Per brevi descrizioni delle proprietà delle informazioni di riepilogo usate con database, trasformazioni e patch, vedere [Descrizioni delle proprietà di riepilogo.](summary-property-descriptions.md)

 

 



