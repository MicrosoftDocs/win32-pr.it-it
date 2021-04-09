---
description: La \_ categoria sensore categoria \_ Light contiene sensori che forniscono informazioni sulle caratteristiche di Light.
ms.assetid: 0327bda5-f1d7-476d-9f0f-f4d60a6a106f
title: SENSOR_CATEGORY_LIGHT (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca14bba297a8f445312873fc810e7d0b5ba13a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878906"
---
# <a name="sensor_category_light"></a><span data-ttu-id="60bae-103">\_categoria sensore \_ chiaro</span><span class="sxs-lookup"><span data-stu-id="60bae-103">SENSOR\_CATEGORY\_LIGHT</span></span>

<span data-ttu-id="60bae-104">La \_ categoria sensore categoria \_ Light contiene sensori che forniscono informazioni sulle caratteristiche di Light.</span><span class="sxs-lookup"><span data-stu-id="60bae-104">The SENSOR\_CATEGORY\_LIGHT category contains sensors that provide information about characteristics of light.</span></span>

<span data-ttu-id="60bae-105">**Tipi di sensore definiti dalla piattaforma**</span><span class="sxs-lookup"><span data-stu-id="60bae-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="60bae-106">Questa categoria include i tipi di sensore definiti dalla piattaforma seguenti.</span><span class="sxs-lookup"><span data-stu-id="60bae-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="60bae-107">Tipo di sensore</span><span class="sxs-lookup"><span data-stu-id="60bae-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="60bae-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60bae-108">Description</span></span>                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|
| <span id="SENSOR_TYPE_AMBIENT_LIGHT"></span><span id="sensor_type_ambient_light"></span><dl> <span data-ttu-id="60bae-109"><dt>**Sensore \_ di TIPO \_ \_ luce ambiente**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt></span><span class="sxs-lookup"><span data-stu-id="60bae-109"><dt>**SENSOR\_TYPE\_AMBIENT\_LIGHT**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt></span></span> </dl> | <span data-ttu-id="60bae-110">Sensori di luce di ambiente.</span><span class="sxs-lookup"><span data-stu-id="60bae-110">Ambient light sensors.</span></span><br/> |



<span data-ttu-id="60bae-111">**Campi dati definiti dalla piattaforma**</span><span class="sxs-lookup"><span data-stu-id="60bae-111">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="60bae-112">Le chiavi di proprietà definite dalla piattaforma per questa categoria sono basate \_ sul \_ tipo di dati GUID luce del sensore \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="60bae-112">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_LIGHT\_GUID:</span></span>

<span data-ttu-id="60bae-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span><span class="sxs-lookup"><span data-stu-id="60bae-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span></span>

<span data-ttu-id="60bae-114">Questa categoria include i campi dati definiti dalla piattaforma seguenti.</span><span class="sxs-lookup"><span data-stu-id="60bae-114">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="60bae-115">Nome del campo dati e PID</span><span class="sxs-lookup"><span data-stu-id="60bae-115">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="60bae-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60bae-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_LIGHT_CHROMACITY__"></span><span id="sensor_data_type_light_chromacity__"></span><dl> <span data-ttu-id="60bae-117"><dt> **Tipo di dati del sensore \_ \_ \_ Light \_ CHROMACITY**</dt> <dt>(PID = 4)</dt></span><span class="sxs-lookup"><span data-stu-id="60bae-117"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_CHROMACITY** </dt> <dt> (PID = 4) </dt></span></span> </dl>                     | <span data-ttu-id="60bae-118">**VT \_ vettore \| VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="60bae-118">**VT\_VECTOR\|VT\_UI1**</span></span><br/> <span data-ttu-id="60bae-119">Cromaticità come matrice calcolata di valori float.</span><span class="sxs-lookup"><span data-stu-id="60bae-119">Chromaticity as a counted array of float values.</span></span><br/> <span data-ttu-id="60bae-120">I dati per i tipi di vettore vengono sempre serializzati come **VT \_ Ui1** (una matrice di caratteri senza segno a 1 byte).</span><span class="sxs-lookup"><span data-stu-id="60bae-120">Data for vector types is always serialized as **VT\_UI1** (an array of unsigned, 1-byte characters).</span></span> <span data-ttu-id="60bae-121">Questo campo dati contiene effettivamente ogni valore come valore reale IEEE a 4 byte (**VT \_ R4**).</span><span class="sxs-lookup"><span data-stu-id="60bae-121">This data field actually contains each value as an IEEE 4-byte real value (**VT\_R4**).</span></span><br/> <span data-ttu-id="60bae-122">Per informazioni sull'utilizzo delle matrici, vedere [recupero di tipi di vettori](retrieving-vector-types.md).</span><span class="sxs-lookup"><span data-stu-id="60bae-122">For information about working with arrays, see [Retrieving Vector Types](retrieving-vector-types.md).</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX"></span><span id="sensor_data_type_light_level_lux"></span><dl> <span data-ttu-id="60bae-123"><dt>**Sensore \_ di Tipo di dati \_ \_ \_ livello leggero \_ Lux**</dt> <dt> (PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="60bae-123"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_LEVEL\_LUX**</dt> <dt> (PID = 2) </dt></span></span> </dl>                            | <span data-ttu-id="60bae-124">**\_R4 VT**</span><span class="sxs-lookup"><span data-stu-id="60bae-124">**VT\_R4**</span></span><br/> <span data-ttu-id="60bae-125">Livello di illuminazione, in Lux.</span><span class="sxs-lookup"><span data-stu-id="60bae-125">Illuminance level, in lux.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_LIGHT_TEMPERATURE_KELVIN"></span><span id="sensor_data_type_light_temperature_kelvin"></span><dl> <span data-ttu-id="60bae-126"><dt>**Sensore \_ di \_Temperatura luce tipo di dati \_ \_ \_ Kelvin**</dt> <dt> (PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="60bae-126"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_TEMPERATURE\_KELVIN**</dt> <dt> (PID = 3) </dt></span></span> </dl> | <span data-ttu-id="60bae-127">**\_R4 VT**</span><span class="sxs-lookup"><span data-stu-id="60bae-127">**VT\_R4**</span></span><br/> <span data-ttu-id="60bae-128">Temperatura del colore, in gradi Kelvin.</span><span class="sxs-lookup"><span data-stu-id="60bae-128">Color temperature, in degrees Kelvin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="60bae-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60bae-129">Requirements</span></span>



| <span data-ttu-id="60bae-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="60bae-130">Requirement</span></span> | <span data-ttu-id="60bae-131">Valore</span><span class="sxs-lookup"><span data-stu-id="60bae-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="60bae-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60bae-132">Minimum supported client</span></span><br/> | <span data-ttu-id="60bae-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="60bae-133">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="60bae-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60bae-134">Minimum supported server</span></span><br/> | <span data-ttu-id="60bae-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="60bae-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="60bae-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60bae-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="60bae-137"><dt>Sensori. h</dt></span><span class="sxs-lookup"><span data-stu-id="60bae-137"><dt>Sensors.h</dt></span></span> </dl> |



 

 




