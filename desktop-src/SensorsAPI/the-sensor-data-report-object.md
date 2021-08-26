---
description: L'oggetto report dei dati del sensore contiene i dati del sensore.
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: Oggetto report dei dati del sensore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca1a8e5f61b23753437bd8b1cf4c2a176515b7042b21e84c4d2f431debc8fe6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992601"
---
# <a name="the-sensor-data-report-object"></a>Oggetto report dei dati del sensore

L'oggetto report dei dati del sensore contiene i dati del sensore.

Per essere utile, un sensore deve fornire dati significativi. La quantità e la frequenza di generazione dei dati variano da sensore a sensore. Ad esempio, un sensore che rileva se una porta è aperta genererebbe una piccola quantità di dati **booleani,** mentre un sensore di movimento potrebbe generare continuamente più elementi di dati. Per standardizzare la modalità di ricezione dei dati da parte del programma, l'API Sensor usa l'oggetto report dei dati del sensore.

È possibile accedere alle informazioni in un report dei dati del sensore tramite [**l'interfaccia ISensorDataReport.**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) Questa interfaccia consente di recuperare il timestamp del report di dati in modo da determinare se le informazioni nel report sono utili. È possibile recuperare i dati stessi in due modi: come valore di un singolo campo dati o come set di valori. Per recuperare i dati come singolo valore, chiamare il [**metodo GetSensorValue.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) Per recuperare più valori, chiamare il [**metodo GetSensorValues.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues)

Specificare il tipo di dati, o campi dati, che si desidera recuperare dal report usando una **costante PROPERTYKEY.** Le chiavi di proprietà per i campi dati di tipi di sensori comuni sono definite in Sensors.h.

 

 
