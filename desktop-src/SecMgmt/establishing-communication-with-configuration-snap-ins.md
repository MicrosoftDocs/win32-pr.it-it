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
# <a name="establishing-communication-with-configuration-snap-ins"></a>Creazione della comunicazione con gli snap-in di configurazione

Dopo che l'estensione dello snap-in allegato è stata aggiunta al nodo servizi, è necessario stabilire una comunicazione con lo snap-in Configurazione sicurezza. Questa operazione è necessaria perché l'estensione dello snap-in allegati ottiene i dati, nonché le modifiche apportate dall'utente, dallo snap-in Configurazione sicurezza. Questa operazione può essere eseguita come descritto nella procedura seguente.

**Per stabilire la comunicazione con gli snap-in configurazione di sicurezza**

1.  Ottenere il nome del file di configurazione usando \_ il \_ formato SCESVC degli Appunti allegati CCF, che restituisce il nome del file di configurazione come **PWSTR**.

    Se l'allegato viene inserito in un nodo del tipo di configurazione, è necessario che l'allegato conosca la configurazione. Comunica queste informazioni agli snap-in di configurazione della sicurezza durante l'inizializzazione dell'interfaccia. In questo caso, usare il codice seguente.

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  Configurare il contesto con gli snap-in configurazione di sicurezza. Dopo che il nome della configurazione è noto o se il nodo del servizio è un nodo di analisi, l'estensione dello snap-in allegato deve chiamare [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) per configurare il contesto, come illustrato nell'esempio seguente.

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
> Al termine dell'utilizzo dell'handle restituito da [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), chiudere l'handle chiamando la funzione [**ISceSvcAttachmentData:: CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) . Questa operazione viene in genere eseguita quando l'utente chiude la console MMC.

 

 

 



