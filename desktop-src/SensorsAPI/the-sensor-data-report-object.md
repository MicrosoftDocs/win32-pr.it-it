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
# <a name="the-sensor-data-report-object"></a><span data-ttu-id="73936-103">Oggetto report dati sensori</span><span class="sxs-lookup"><span data-stu-id="73936-103">The Sensor Data Report Object</span></span>

<span data-ttu-id="73936-104">L'oggetto report dati sensori contiene i dati del sensore.</span><span class="sxs-lookup"><span data-stu-id="73936-104">The sensor data report object contains sensor data.</span></span>

<span data-ttu-id="73936-105">Affinché un sensore sia utile, deve fornire dati significativi.</span><span class="sxs-lookup"><span data-stu-id="73936-105">For a sensor to be useful, it must provide meaningful data.</span></span> <span data-ttu-id="73936-106">La quantità e la frequenza di generazione dei dati variano da sensore a sensore.</span><span class="sxs-lookup"><span data-stu-id="73936-106">The amount and frequency of data generation varies from sensor to sensor.</span></span> <span data-ttu-id="73936-107">Ad esempio, un sensore che rileva se uno sportello è aperto genera una piccola quantità di dati **booleani** , mentre un sensore di movimento può generare continuamente più elementi di dati.</span><span class="sxs-lookup"><span data-stu-id="73936-107">For example, a sensor that detects whether a door is open would generate a small amount of **Boolean** data, while a motion sensor might continuously generate multiple data items.</span></span> <span data-ttu-id="73936-108">Per standardizzare la modalità di ricezione dei dati da parte del programma, l'API Sensor usa l'oggetto report dati sensori.</span><span class="sxs-lookup"><span data-stu-id="73936-108">To standardize the way your program receives data, the Sensor API uses the sensor data report object.</span></span>

<span data-ttu-id="73936-109">È possibile accedere alle informazioni in un report sui dati dei sensori tramite l'interfaccia [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) .</span><span class="sxs-lookup"><span data-stu-id="73936-109">You can access the information in a sensor data report through the [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) interface.</span></span> <span data-ttu-id="73936-110">Questa interfaccia consente di recuperare il timestamp del report dati in modo che sia possibile determinare se le informazioni del report sono utili.</span><span class="sxs-lookup"><span data-stu-id="73936-110">This interface lets you retrieve the data report's time stamp so that you can determine whether the information in the report is useful.</span></span> <span data-ttu-id="73936-111">È possibile recuperare i dati in due modi: come singolo valore del campo dati o come set di valori.</span><span class="sxs-lookup"><span data-stu-id="73936-111">You can retrieve the data itself in two ways: as an individual data field value or as a set of values.</span></span> <span data-ttu-id="73936-112">Per recuperare i dati come singolo valore, chiamare il metodo [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) .</span><span class="sxs-lookup"><span data-stu-id="73936-112">To retrieve data as an individual value, call the [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) method.</span></span> <span data-ttu-id="73936-113">Per recuperare più valori, chiamare il metodo [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) .</span><span class="sxs-lookup"><span data-stu-id="73936-113">To retrieve multiple values, call the [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) method.</span></span>

<span data-ttu-id="73936-114">È possibile specificare il tipo di dati o i campi dati che si desidera recuperare dal report utilizzando una costante **PropertyKey** .</span><span class="sxs-lookup"><span data-stu-id="73936-114">You specify the type of data, or data fields, that you want to retrieve from the report by using a **PROPERTYKEY** constant.</span></span> <span data-ttu-id="73936-115">Le chiavi di proprietà per i campi dati dei tipi di sensori comuni sono definite in sensors. h.</span><span class="sxs-lookup"><span data-stu-id="73936-115">Property keys for data fields of common sensor types are defined in Sensors.h.</span></span>

 

 
