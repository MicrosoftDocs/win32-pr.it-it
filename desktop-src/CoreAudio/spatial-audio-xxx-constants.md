---
description: Le \_ \_ costanti xxx audio spaziali definiscono i valori relativi alle funzionalità audio spaziali.
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: Costanti SPATIAL_AUDIO_XXX (SpatialAudioMetadata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2c92b970f69cf84e0744f21a41932a8851efed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331295"
---
# <a name="spatial_audio_xxx-constants"></a><span data-ttu-id="c8159-103">\_ \_ Costanti xxx audio spaziali</span><span class="sxs-lookup"><span data-stu-id="c8159-103">SPATIAL\_AUDIO\_XXX Constants</span></span>

<span data-ttu-id="c8159-104">Le \_ \_ costanti xxx audio spaziali definiscono i valori relativi alle funzionalità audio spaziali.</span><span class="sxs-lookup"><span data-stu-id="c8159-104">The SPATIAL\_AUDIO\_XXX constants define values related to spatial sound features.</span></span>



| <span data-ttu-id="c8159-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="c8159-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="c8159-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8159-106">Description</span></span>                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <span data-ttu-id="c8159-107"><dt>**Spaziale \_ \_Posizione AUDIO**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="c8159-107"><dt>**SPATIAL\_AUDIO\_POSITION**</dt> <dt>200</dt></span></span> </dl>                                                   | <span data-ttu-id="c8159-108">Comando standard di metadati audio spaziali definito da Microsoft che rappresenta la posizione del listener nel modello standard usato da [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) in cui la testa del listener è posizionata in corrispondenza delle coordinate (0, 0, 0), definita in metri.</span><span class="sxs-lookup"><span data-stu-id="c8159-108">A standard Microsoft-defined spatial audio metadata command which represents the listener position in the standard model used by [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) where the listener's head is position at coordinates (0,0,0), defined in meters.</span></span><br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <span data-ttu-id="c8159-109"><dt>**Spaziale \_ \_ \_ \_ Conteggio byte posizione audio**</dt> <dt>sizeof (float) \* 3</dt></span><span class="sxs-lookup"><span data-stu-id="c8159-109"><dt>**SPATIAL\_AUDIO\_POSITION\_BYTE\_COUNT**</dt> <dt>sizeof(float) \* 3</dt></span></span> </dl> | <span data-ttu-id="c8159-110">Specifica la dimensione del valore **della \_ \_ posizione audio spaziale** .</span><span class="sxs-lookup"><span data-stu-id="c8159-110">Specifies the size of the **SPATIAL\_AUDIO\_POSITION** value.</span></span><br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <span data-ttu-id="c8159-111"><dt>**Spaziale \_ \_Comandi audio \_ standard \_ avviati**</dt> <dt>200</dt></span><span class="sxs-lookup"><span data-stu-id="c8159-111"><dt>**SPATIAL\_AUDIO\_STANDARD\_COMMANDS\_START**</dt> <dt>200</dt></span></span> </dl>    | <span data-ttu-id="c8159-112">Specifica l'inizio dell'intervallo dei comandi di metadati audio spaziali riservati a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c8159-112">Specifies the start of the range of Microsoft-reserved spatial audio metadata commands.</span></span> <span data-ttu-id="c8159-113">I comandi dei metadati personalizzati sono limitati agli ID di comando 0-199.</span><span class="sxs-lookup"><span data-stu-id="c8159-113">Custom metadata commands are restricted to command IDs 0 - 199.</span></span> <span data-ttu-id="c8159-114">I comandi 200-255 sono riservati per l'uso da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c8159-114">Commands 200 - 255 are reserved for Microsoft use.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="c8159-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8159-115">Requirements</span></span>



| <span data-ttu-id="c8159-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8159-116">Requirement</span></span> | <span data-ttu-id="c8159-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c8159-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8159-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8159-118">Header</span></span><br/> | <dl> <span data-ttu-id="c8159-119"><dt>SpatialAudioMetadata. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8159-119"><dt>SpatialAudioMetadata.h</dt></span></span> </dl> |



 

 




