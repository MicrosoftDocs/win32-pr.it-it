---
description: Il flusso di informazioni di riepilogo contiene informazioni sul pacchetto che possono essere visualizzate tramite Esplora risorse di Microsoft Windows.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: Informazioni sul flusso di informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131510"
---
# <a name="about-the-summary-information-stream"></a>Informazioni sul flusso di informazioni di riepilogo

Il flusso di informazioni di riepilogo contiene informazioni sul pacchetto che possono essere visualizzate tramite Esplora risorse di Microsoft Windows. Queste informazioni sono accessibili tramite l'interfaccia **IStream** . Spetta all'autore specificare i valori per ognuna di queste proprietà.

Il flusso di informazioni di riepilogo USA COM per fornire l'archiviazione strutturata dei database. COM supporta il concetto di archiviazione strutturata accessibile tramite l'interfaccia **IStream** . L'archiviazione strutturata, a sua volta, supporta il concetto di set di proprietà come metodo flessibile per la serializzazione di quasi tutte le informazioni. La specifica COM definisce un singolo set di proprietà standard, informazioni di riepilogo, utilizzato per popolare le finestre delle proprietà visualizzabili da Esplora risorse. Quindi, le informazioni archiviate nel flusso di informazioni di riepilogo possono essere visualizzate dagli utenti facendo clic con il pulsante destro del mouse su un database del programma di installazione o una trasformazione e selezionando [Proprietà](about-properties.md).

Per un elenco del set di proprietà di riepilogo, vedere [set di proprietà del flusso di informazioni di riepilogo](summary-information-stream-property-set.md).

Per brevi descrizioni delle proprietà delle informazioni di riepilogo usate con i database, le trasformazioni e le patch, vedere [descrizioni delle proprietà di riepilogo](summary-property-descriptions.md).

 

 



