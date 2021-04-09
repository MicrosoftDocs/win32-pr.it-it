---
description: La \_ categoria Sensor \_ All rappresenta il set di tutte le categorie di sensori definite dalla piattaforma.
ms.assetid: e2d9fe6d-450a-446b-968b-0924116af6fe
title: SENSOR_CATEGORY_ALL (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2e5641e51dde130cc51d9b2fc35fcc1e158ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750818"
---
# <a name="sensor_category_all"></a><span data-ttu-id="f059b-103">\_categoria sensore \_ tutti</span><span class="sxs-lookup"><span data-stu-id="f059b-103">SENSOR\_CATEGORY\_ALL</span></span>

<span data-ttu-id="f059b-104">La \_ categoria Sensor \_ All rappresenta il set di tutte le categorie di sensori definite dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f059b-104">The SENSOR\_CATEGORY\_ALL category represents the set of all platform-defined sensor categories.</span></span>

<span data-ttu-id="f059b-105">**Chiavi di proprietà definite dalla piattaforma**</span><span class="sxs-lookup"><span data-stu-id="f059b-105">**Platform-Defined Property Keys**</span></span>

<span data-ttu-id="f059b-106">Le chiavi delle proprietà definite dalla piattaforma per questa categoria sono basate \_ sul \_ GUID comune del tipo di dati del sensore \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="f059b-106">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_COMMON\_GUID:</span></span>

<span data-ttu-id="f059b-107">{DB5E0CF2-CF1F-4C18-B46C-D86011D62150}</span><span class="sxs-lookup"><span data-stu-id="f059b-107">{DB5E0CF2-CF1F-4C18-B46C-D86011D62150}</span></span>

<span data-ttu-id="f059b-108">Nella tabella seguente vengono descritti i campi dati definiti dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f059b-108">The following table describes platform-defined data fields.</span></span>



| <span data-ttu-id="f059b-109">Nome del campo dati e PID</span><span class="sxs-lookup"><span data-stu-id="f059b-109">Data field name and PID</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="f059b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f059b-110">Description</span></span>                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_TIMESTAMP"></span><span id="sensor_data_type_timestamp"></span><dl> <span data-ttu-id="f059b-111"><dt>**Sensore \_ di \_ \_ Timestamp del tipo di dati**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="f059b-111"><dt>**SENSOR\_DATA\_TYPE\_TIMESTAMP**</dt> <dt>(PID = 2 ) </dt></span></span> </dl> | <span data-ttu-id="f059b-112">**FILETIME VT \_**</span><span class="sxs-lookup"><span data-stu-id="f059b-112">**VT\_FILETIME**</span></span><br/> <span data-ttu-id="f059b-113">Obbligatorio per tutti i report di dati.</span><span class="sxs-lookup"><span data-stu-id="f059b-113">Required for all data reports.</span></span> <span data-ttu-id="f059b-114">Contrassegna ogni report dei dati con l'ora in cui è stato creato il report dati nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="f059b-114">Marks each data report with the time the data report was created in Coordinated Universal Time (UTC) format.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f059b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f059b-115">Requirements</span></span>



| <span data-ttu-id="f059b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f059b-116">Requirement</span></span> | <span data-ttu-id="f059b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f059b-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f059b-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f059b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f059b-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f059b-119">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f059b-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f059b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f059b-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f059b-121">None supported</span></span><br/>                                                            |
| <span data-ttu-id="f059b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f059b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f059b-123"><dt>Sensori. h</dt></span><span class="sxs-lookup"><span data-stu-id="f059b-123"><dt>Sensors.h</dt></span></span> </dl> |



 

 




