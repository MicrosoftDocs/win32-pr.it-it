---
description: La \_ categoria Sensor Category \_ scanner contiene sensori che forniscono informazioni ottenute tramite l'analisi.
ms.assetid: 98a772c9-2a21-489f-ad8d-3b772b7ff892
title: SENSOR_CATEGORY_SCANNER (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b38fdb3358ff3ce2ae96ce901972cc6842a0d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966572"
---
# <a name="sensor_category_scanner"></a><span data-ttu-id="c658d-103">\_scanner categoria \_ sensori</span><span class="sxs-lookup"><span data-stu-id="c658d-103">SENSOR\_CATEGORY\_SCANNER</span></span>

<span data-ttu-id="c658d-104">La \_ categoria Sensor Category \_ scanner contiene sensori che forniscono informazioni ottenute tramite l'analisi.</span><span class="sxs-lookup"><span data-stu-id="c658d-104">The SENSOR\_CATEGORY\_SCANNER category contains sensors that provide information that is obtained by scanning.</span></span>

<span data-ttu-id="c658d-105">**Tipi di sensore definiti dalla piattaforma**</span><span class="sxs-lookup"><span data-stu-id="c658d-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="c658d-106">Questa categoria include i tipi di sensore definiti dalla piattaforma seguenti.</span><span class="sxs-lookup"><span data-stu-id="c658d-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="c658d-107">Tipo di sensore</span><span class="sxs-lookup"><span data-stu-id="c658d-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="c658d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c658d-108">Description</span></span>                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="SENSOR_TYPE_BARCODE_SCANNER"></span><span id="sensor_type_barcode_scanner"></span><dl> <span data-ttu-id="c658d-109"><dt>**Sensore \_ di Digitare \_ Barcode \_ scanner**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt></span><span class="sxs-lookup"><span data-stu-id="c658d-109"><dt>**SENSOR\_TYPE\_BARCODE\_SCANNER**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt></span></span> </dl> | <span data-ttu-id="c658d-110">Sensori che usano l'analisi ottica per leggere i codici a barre.</span><span class="sxs-lookup"><span data-stu-id="c658d-110">Sensors that use optical scanning to read bar codes.</span></span><br/> |
| <span id="SENSOR_TYPE_RFID_SCANNER"></span><span id="sensor_type_rfid_scanner"></span><dl> <span data-ttu-id="c658d-111"><dt>**Sensore \_ di Digitare \_ RFID \_ scanner**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt></span><span class="sxs-lookup"><span data-stu-id="c658d-111"><dt>**SENSOR\_TYPE\_RFID\_SCANNER**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt></span></span> </dl>          | <span data-ttu-id="c658d-112">Sensori di scansione con ID frequenza radio.</span><span class="sxs-lookup"><span data-stu-id="c658d-112">Radio-frequency ID scanning sensors.</span></span><br/>                 |



<span data-ttu-id="c658d-113">**Campi dati definiti dalla piattaforma**</span><span class="sxs-lookup"><span data-stu-id="c658d-113">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="c658d-114">Le chiavi delle proprietà definite dalla piattaforma per questa categoria sono basate \_ sul \_ \_ GUID dello scanner del tipo di dati del sensore \_ :</span><span class="sxs-lookup"><span data-stu-id="c658d-114">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_SCANNER\_GUID:</span></span>

<span data-ttu-id="c658d-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span><span class="sxs-lookup"><span data-stu-id="c658d-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span></span>

<span data-ttu-id="c658d-116">Questa categoria include i campi dati definiti dalla piattaforma seguenti.</span><span class="sxs-lookup"><span data-stu-id="c658d-116">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="c658d-117">Nome del campo dati e PID</span><span class="sxs-lookup"><span data-stu-id="c658d-117">Data field name and PID</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="c658d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c658d-118">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_RFID_TAG_40_BIT"></span><span id="sensor_data_type_rfid_tag_40_bit"></span><dl> <span data-ttu-id="c658d-119"><dt>**Sensore \_ di Tipo di dati \_ \_ \_ tag RFID \_ 40 \_ bit**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="c658d-119"><dt>**SENSOR\_DATA\_TYPE\_RFID\_TAG\_40\_BIT**</dt> <dt>(PID = 2) </dt></span></span> </dl> | <span data-ttu-id="c658d-120">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="c658d-120">**VT\_UI8**</span></span><br/> <span data-ttu-id="c658d-121">valore del tag ID frequenza radio a 40 bit.</span><span class="sxs-lookup"><span data-stu-id="c658d-121">40-bit radio frequency ID tag value.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c658d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c658d-122">Requirements</span></span>



| <span data-ttu-id="c658d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c658d-123">Requirement</span></span> | <span data-ttu-id="c658d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c658d-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c658d-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c658d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c658d-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c658d-126">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c658d-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c658d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c658d-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c658d-128">None supported</span></span><br/>                                                            |
| <span data-ttu-id="c658d-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c658d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c658d-130"><dt>Sensori. h</dt></span><span class="sxs-lookup"><span data-stu-id="c658d-130"><dt>Sensors.h</dt></span></span> </dl> |



 

 




