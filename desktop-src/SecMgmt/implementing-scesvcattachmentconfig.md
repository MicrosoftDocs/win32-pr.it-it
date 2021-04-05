---
description: È necessario recuperare le informazioni dal database di sicurezza e quindi utilizzare tali informazioni per configurare il servizio.
ms.assetid: c0c1c1e4-de5b-405d-abe8-33a985ce98e5
title: Implementazione di SceSvcAttachmentConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98eb519e6422e3036ddfb203811322befd2713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968007"
---
# <a name="implementing-scesvcattachmentconfig"></a><span data-ttu-id="007a0-103">Implementazione di SceSvcAttachmentConfig</span><span class="sxs-lookup"><span data-stu-id="007a0-103">Implementing SceSvcAttachmentConfig</span></span>

<span data-ttu-id="007a0-104">La funzione [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) deve recuperare le informazioni dal database di sicurezza e quindi utilizzare tali informazioni per configurare il servizio.</span><span class="sxs-lookup"><span data-stu-id="007a0-104">The [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) function must retrieve information from the security database and then use that information to configure the service.</span></span>

<span data-ttu-id="007a0-105">Quando si implementa [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), è possibile recuperare tutte le informazioni e quindi configurare il servizio oppure recuperare e configurare il servizio in passaggi.</span><span class="sxs-lookup"><span data-stu-id="007a0-105">When implementing [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), you can either retrieve all of the information and then configure the service, or retrieve and configure the service in steps.</span></span> <span data-ttu-id="007a0-106">Nell'algoritmo seguente vengono recuperate tutte le informazioni e quindi viene configurato il servizio.</span><span class="sxs-lookup"><span data-stu-id="007a0-106">The following algorithm retrieves all of the information and then configures the service.</span></span>

<span data-ttu-id="007a0-107">**Per implementare SceSvcAttachmentConfig**</span><span class="sxs-lookup"><span data-stu-id="007a0-107">**To implement SceSvcAttachmentConfig**</span></span>

1.  <span data-ttu-id="007a0-108">Definire le variabili necessarie per recuperare le informazioni e i codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="007a0-108">Define the variables needed to retrieve information and return codes.</span></span>
2.  <span data-ttu-id="007a0-109">Chiamare la funzione di callback pfQueryInfo nella struttura di callback per recuperare le informazioni di configurazione dal database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="007a0-109">Call the pfQueryInfo callback function in the callback structure to retrieve configuration information from the security database.</span></span>
3.  <span data-ttu-id="007a0-110">Configurare il sistema con le informazioni restituite.</span><span class="sxs-lookup"><span data-stu-id="007a0-110">Configure the system with the returned information.</span></span>
4.  <span data-ttu-id="007a0-111">Chiamare la funzione di callback pfFreeInfo nella struttura di callback per liberare la memoria utilizzata per le informazioni restituite.</span><span class="sxs-lookup"><span data-stu-id="007a0-111">Call the pfFreeInfo callback function in the callback structure to free memory used for returned information.</span></span>
5.  <span data-ttu-id="007a0-112">Se è presente un messaggio che l'estensione desidera aggiungere al file di log di analisi, chiamare la funzione di callback pfLogInfo nella struttura di callback.</span><span class="sxs-lookup"><span data-stu-id="007a0-112">If there is any message that the extension wants to add to the analysis log file, call the pfLogInfo callback function in the callback structure.</span></span>
6.  <span data-ttu-id="007a0-113">Restituisce i codici **SCESTATUS** appropriati.</span><span class="sxs-lookup"><span data-stu-id="007a0-113">Return the appropriate **SCESTATUS** codes.</span></span>

<span data-ttu-id="007a0-114">Nell'esempio seguente viene illustrata una possibile implementazione di [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md).</span><span class="sxs-lookup"><span data-stu-id="007a0-114">The following example shows one possible implementation of [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md).</span></span> <span data-ttu-id="007a0-115">Si noti che in questo esempio la funzione ProcessConfigurationLine imposta la configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="007a0-115">Note that in this example, the function ProcessConfigurationLine sets the service configuration.</span></span> <span data-ttu-id="007a0-116">L'implementazione di questa funzione non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="007a0-116">The implementation of this function is not shown.</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig (
    IN PSCESVC_CALLBACK_INFO pSceCbInfo
)
{
  
  ////////////////////////////////////////////////////
  // Define variables.
  ////////////////////////////////////////////////////
     PSCESVC_CONFIGURATION_INFO     pConfigInfo = NULL;
     SCESTATUS                      retCode;
     SCE_ENUMERATION_CONTEXT        EnumContext = 0;
  
     if ( pSceCbInfo == NULL ||
         pSceCbInfo->sceHandle == NULL ||
         pSceCbInfo->pfQueryInfo == NULL ||
         pSceCbInfo->pfSetInfo == NULL ||
         pSceCbInfo->pfFreeInfo == NULL ) 
     {
        return(SCESTATUS_INVALID_PARAMETER);
     }
  
  
      ////////////////////////////////////////////////////
      // Retrieve configuration information and configure
      // system. 
      ////////////////////////////////////////////////////
      do
      {
            retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                                  SceSvcConfigurationInfo,
                                  NULL,
                                  FALSE,
                                  (PVOID *)&pConfigInfo,
                                  &EnumContext
                                 );
            if (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
            {
              ULONG i:
              //////////////////////////////////////////////////
              // Configure system.
              /////////////////////////////////////////////////
              for(i = 0; < pConfigInfo->Count; i++)
              {
                if(pConfigInfo->Line[i].Key == NULL) 
                    continue;
                ProcessConfigurationLine(pConfigInfo->Line[i]);
              }
      
      
              //////////////////////////////////////////////////
              // Free data returned.
              /////////////////////////////////////////////////
              (*(pSceCbInfo->pfFreeInfo)) ((PVOPID)pConfigInfo);
              pConfigInfo = NULL;
            }
        } while (retCode == SCESTATUS_SUCCESS && CountReturned > 0);
  
  
  ////////////////////////////////////////////////////
  // Add code for other return codes if retCode is 
  // not SCESTATUS_SUCCESS.
  ///////////////////////////////////////////////////
  return retCode;
}
```



 

 



