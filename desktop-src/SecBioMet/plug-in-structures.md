---
title: Strutture di plug-in
description: Strutture per lo sviluppo di applicazioni client da parte dell'API Windows Biometric Framework.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- API Windows Biometric Framework API di Windows Biometric Framework, strutture di plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193b5a99f30c76e8e6e2ab7ebf0242cf56905816
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331671"
---
# <a name="plug-in-structures"></a><span data-ttu-id="faf35-104">Strutture di plug-in</span><span class="sxs-lookup"><span data-stu-id="faf35-104">Plug-in Structures</span></span>

<span data-ttu-id="faf35-105">Le strutture seguenti sono supportate per lo sviluppo di applicazioni client da parte dell'API Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="faf35-105">The following structures are supported for client application development by the Windows Biometric Framework API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="faf35-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="faf35-106">In this section</span></span>



| <span data-ttu-id="faf35-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="faf35-107">Topic</span></span>                                                                                                | <span data-ttu-id="faf35-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faf35-108">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="faf35-109">**\_criteri dell'account WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="faf35-109">**WINBIO\_ACCOUNT\_POLICY**</span></span>](winbio-account-policy.md)<br/>                                  | <span data-ttu-id="faf35-110">Contiene criteri di antispoofing predefiniti o specifici dell'account.</span><span class="sxs-lookup"><span data-stu-id="faf35-110">Contains either a default or account-specific antispoofing policy.</span></span><br/>                                                         |
| [<span data-ttu-id="faf35-111">**\_versione dell' \_ interfaccia dell'adattatore WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="faf35-111">**WINBIO\_ADAPTER\_INTERFACE\_VERSION**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | <span data-ttu-id="faf35-112">Contiene un numero di versione principale e secondario utilizzato nelle tabelle di interfaccia del motore, del sensore e dell'adattatore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="faf35-112">Contains a major and minor version number used in the engine, sensor, and storage adapter interface tables.</span></span><br/>                |
| [<span data-ttu-id="faf35-113">**\_interfaccia del motore WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="faf35-113">**WINBIO\_ENGINE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | <span data-ttu-id="faf35-114">Contiene i puntatori alle funzioni dell'adattatore del motore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="faf35-114">Contains pointers to your custom engine adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="faf35-115">**WINBIO \_ parametri di registrazione estesi \_ \_**</span><span class="sxs-lookup"><span data-stu-id="faf35-115">**WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS**</span></span>](winbio-extended-enrollment-parameters.md)<br/> | <span data-ttu-id="faf35-116">Contiene informazioni aggiuntive necessarie per la creazione di un modello di registrazione da un adattatore del motore.</span><span class="sxs-lookup"><span data-stu-id="faf35-116">Contains additional information that an engine adapter needs to create an enrollment template.</span></span> <br/>                            |
| [<span data-ttu-id="faf35-117">**\_pipeline WINBIO**</span><span class="sxs-lookup"><span data-stu-id="faf35-117">**WINBIO\_PIPELINE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | <span data-ttu-id="faf35-118">Contiene informazioni di contesto condivise utilizzate dal sensore, dal motore e dai componenti dell'adattatore di archiviazione in un'unica unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="faf35-118">Contains shared context information used by the sensor, engine, and storage adapter components in a single biometric unit.</span></span><br/> |
| [<span data-ttu-id="faf35-119">**\_interfaccia del sensore WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="faf35-119">**WINBIO\_SENSOR\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | <span data-ttu-id="faf35-120">Contiene i puntatori alle funzioni dell'adattatore del sensore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="faf35-120">Contains pointers to your custom sensor adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="faf35-121">**\_interfaccia di archiviazione WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="faf35-121">**WINBIO\_STORAGE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | <span data-ttu-id="faf35-122">Contiene i puntatori alle funzioni dell'adattatore di archiviazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="faf35-122">Contains pointers to your custom storage adapter functions.</span></span><br/>                                                                |
| [<span data-ttu-id="faf35-123">**\_record di archiviazione WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="faf35-123">**WINBIO\_STORAGE\_RECORD**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | <span data-ttu-id="faf35-124">Contiene un modello biometrico e i dati associati in un formato standard.</span><span class="sxs-lookup"><span data-stu-id="faf35-124">Contains a biometric template and associated data in a standard format.</span></span><br/>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="faf35-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="faf35-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faf35-126">Riferimento al plug-in</span><span class="sxs-lookup"><span data-stu-id="faf35-126">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> <dt>

[<span data-ttu-id="faf35-127">Funzioni plug-in</span><span class="sxs-lookup"><span data-stu-id="faf35-127">Plug-in Functions</span></span>](plug-in-functions.md)
</dt> <dt>

[<span data-ttu-id="faf35-128">**WbioQueryEngineInterface**</span><span class="sxs-lookup"><span data-stu-id="faf35-128">**WbioQueryEngineInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[<span data-ttu-id="faf35-129">**WbioQuerySensorInterface**</span><span class="sxs-lookup"><span data-stu-id="faf35-129">**WbioQuerySensorInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[<span data-ttu-id="faf35-130">**WbioQueryStorageInterface**</span><span class="sxs-lookup"><span data-stu-id="faf35-130">**WbioQueryStorageInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





