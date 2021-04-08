---
description: L'oggetto report dati sensori contiene i dati del sensore.
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: Oggetto report dati sensori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d43753aa28be5cd20c85b7e65bf4c7516d4c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967871"
---
# <a name="the-sensor-data-report-object"></a>Oggetto report dati sensori

L'oggetto report dati sensori contiene i dati del sensore.

Affinché un sensore sia utile, deve fornire dati significativi. La quantità e la frequenza di generazione dei dati variano da sensore a sensore. Ad esempio, un sensore che rileva se uno sportello è aperto genera una piccola quantità di dati **booleani** , mentre un sensore di movimento può generare continuamente più elementi di dati. Per standardizzare la modalità di ricezione dei dati da parte del programma, l'API Sensor usa l'oggetto report dati sensori.

È possibile accedere alle informazioni in un report sui dati dei sensori tramite l'interfaccia [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) . Questa interfaccia consente di recuperare il timestamp del report dati in modo che sia possibile determinare se le informazioni del report sono utili. È possibile recuperare i dati in due modi: come singolo valore del campo dati o come set di valori. Per recuperare i dati come singolo valore, chiamare il metodo [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) . Per recuperare più valori, chiamare il metodo [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) .

È possibile specificare il tipo di dati o i campi dati che si desidera recuperare dal report utilizzando una costante **PropertyKey** . Le chiavi di proprietà per i campi dati dei tipi di sensori comuni sono definite in sensors. h.

 

 
