---
description: "L'estensione dello snap-in allegati non è in grado di eseguire direttamente una query sul database di sicurezza per recuperare le informazioni. Deve invece eseguire una query su queste informazioni dagli snap-in di configurazione della sicurezza usando ISceSvcAttachmentData:: GetData."
ms.assetid: 1171beed-5b28-4f31-b33f-533e3c631b0d
title: Recupero di dati dagli snap-in di configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c888cef92a354f73f01e87fca12cee2567dab48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529640"
---
# <a name="getting-data-from-the-configuration-snap-ins"></a><span data-ttu-id="4af86-104">Recupero di dati dagli snap-in di configurazione</span><span class="sxs-lookup"><span data-stu-id="4af86-104">Getting Data from the Configuration Snap-ins</span></span>

<span data-ttu-id="4af86-105">L'estensione dello snap-in allegati non è in grado di eseguire direttamente una query sul database di sicurezza per recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="4af86-105">The attachment snap-in extension has no way to directly query the security database to retrieve information.</span></span> <span data-ttu-id="4af86-106">Deve invece eseguire una query su queste informazioni dagli snap-in di configurazione della sicurezza usando [**ISceSvcAttachmentData:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span><span class="sxs-lookup"><span data-stu-id="4af86-106">Instead, it must query this information from the Security Configuration snap-ins using [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span></span>

<span data-ttu-id="4af86-107">Lo snap-in allegati può recuperare tutti i dati durante l'inizializzazione oppure può recuperare informazioni quando il relativo nodo è aperto.</span><span class="sxs-lookup"><span data-stu-id="4af86-107">The attachment snap-in can retrieve all of the data when it initializes itself, or it can retrieve information when its node is opened.</span></span>

> [!Note]  
> <span data-ttu-id="4af86-108">È necessario usare il metodo [**ISceSvcAttachmentData:: FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) per liberare il buffer allocato dal metodo di snap-in configurazione di sicurezza [**ISceSvcAttachmentData:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span><span class="sxs-lookup"><span data-stu-id="4af86-108">You must use the [**ISceSvcAttachmentData::FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) method to free the buffer allocated by the Security Configuration snap-in method [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span></span>

 

 

 



