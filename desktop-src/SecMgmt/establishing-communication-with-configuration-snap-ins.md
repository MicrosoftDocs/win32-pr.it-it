---
description: Dopo che l'estensione dello snap-in allegato è stata aggiunta al nodo servizi, è necessario stabilire una comunicazione con lo snap-in Configurazione sicurezza.
ms.assetid: 68a0e5a7-938f-45b7-90a3-8f35e5e6bbfb
title: Creazione della comunicazione con gli snap-in di configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fe9bcb80687fa50120d20594a81ea40b21c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315351"
---
# <a name="establishing-communication-with-configuration-snap-ins"></a><span data-ttu-id="bf647-103">Creazione della comunicazione con gli snap-in di configurazione</span><span class="sxs-lookup"><span data-stu-id="bf647-103">Establishing Communication with Configuration Snap-ins</span></span>

<span data-ttu-id="bf647-104">Dopo che l'estensione dello snap-in allegato è stata aggiunta al nodo servizi, è necessario stabilire una comunicazione con lo snap-in Configurazione sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bf647-104">After your attachment snap-in extension has added itself to the Services node, it should establish communication with the Security Configuration snap-in.</span></span> <span data-ttu-id="bf647-105">Questa operazione è necessaria perché l'estensione dello snap-in allegati ottiene i dati, nonché le modifiche apportate dall'utente, dallo snap-in Configurazione sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bf647-105">This is necessary because the attachment snap-in extension gets its data, as well as any changes made by the user, from the Security Configuration snap-in.</span></span> <span data-ttu-id="bf647-106">Questa operazione può essere eseguita come descritto nella procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="bf647-106">This can be done as described in the following procedure.</span></span>

<span data-ttu-id="bf647-107">**Per stabilire la comunicazione con gli snap-in configurazione di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="bf647-107">**To establish communication with the Security Configuration snap-ins**</span></span>

1.  <span data-ttu-id="bf647-108">Ottenere il nome del file di configurazione usando \_ il \_ formato SCESVC degli Appunti allegati CCF, che restituisce il nome del file di configurazione come **PWSTR**.</span><span class="sxs-lookup"><span data-stu-id="bf647-108">Obtain the configuration file name using the CCF\_SCESVC\_ATTACHMENT clipboard format, which returns the configuration file name as a **PWSTR**.</span></span>

    <span data-ttu-id="bf647-109">Se l'allegato viene inserito in un nodo del tipo di configurazione, è necessario che l'allegato conosca la configurazione.</span><span class="sxs-lookup"><span data-stu-id="bf647-109">If the attachment is inserted under a configuration type node, the attachment needs to know which configuration it is.</span></span> <span data-ttu-id="bf647-110">Comunica queste informazioni agli snap-in di configurazione della sicurezza durante l'inizializzazione dell'interfaccia. In questo caso, usare il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="bf647-110">(It communicates this information to the Security Configuration snap-ins during interface initialization.) In this case, use the following code.</span></span>

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  <span data-ttu-id="bf647-111">Configurare il contesto con gli snap-in configurazione di sicurezza. Dopo che il nome della configurazione è noto o se il nodo del servizio è un nodo di analisi, l'estensione dello snap-in allegato deve chiamare [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) per configurare il contesto, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="bf647-111">Set up the context with the Security Configuration snap-ins. After the configuration name is known, or if the service node is an analysis node, the attachment snap-in extension must call [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) to set up the context, as shown in the following example.</span></span>

    ```C++
    LPSCESVCATTACHMENTPERSISTINFO pSceInfo;

        HRESULT hr = ((LPSCESVCATTACHMENTPERSISTINFO)this)->
                QueryInterface(IID_ISceSvcAttachmentPersistInfo,
                (void**)&pSceInfo);

        if ( SUCCEEDED(hr) )
        {

            hr = m_pSceData->Initialize(strServiceName, TemplateName,
                    pSceInfo, &ThisHandle);
            // Continue processing (not shown).
        }
    ```

    

> [!Note]  
> <span data-ttu-id="bf647-112">Al termine dell'utilizzo dell'handle restituito da [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), chiudere l'handle chiamando la funzione [**ISceSvcAttachmentData:: CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="bf647-112">When you have finished using the handle returned by [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), close the handle by calling the [**ISceSvcAttachmentData::CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) function.</span></span> <span data-ttu-id="bf647-113">Questa operazione viene in genere eseguita quando l'utente chiude la console MMC.</span><span class="sxs-lookup"><span data-stu-id="bf647-113">This is typically done when the user closes the MMC console.</span></span>

 

 

 



