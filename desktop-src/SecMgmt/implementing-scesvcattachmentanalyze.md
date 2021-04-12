---
description: È necessario recuperare le informazioni di configurazione dal database di sicurezza e dal servizio, confrontare i due set di informazioni, quindi aggiornare la sezione di analisi del database di sicurezza con eventuali differenze.
ms.assetid: f8420dde-55a2-40a0-b10d-140c28c0e9e4
title: Implementazione di SceSvcAttachmentAnalyze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f8501be2caac84c3dc96363eb85a8bc787d2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232653"
---
# <a name="implementing-scesvcattachmentanalyze"></a><span data-ttu-id="b1b12-103">Implementazione di SceSvcAttachmentAnalyze</span><span class="sxs-lookup"><span data-stu-id="b1b12-103">Implementing SceSvcAttachmentAnalyze</span></span>

<span data-ttu-id="b1b12-104">La funzione [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md) deve recuperare le informazioni di configurazione dal database di sicurezza e dal servizio, confrontare i due set di informazioni, quindi aggiornare la sezione di analisi del database di sicurezza con eventuali differenze.</span><span class="sxs-lookup"><span data-stu-id="b1b12-104">The [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md) function must retrieve configuration information from the security database and the service, compare the two sets of information, and then update the analysis section of the security database with any differences.</span></span> <span data-ttu-id="b1b12-105">A tale scopo, è possibile usare l'algoritmo seguente:</span><span class="sxs-lookup"><span data-stu-id="b1b12-105">You can ensure this by using the following algorithm.</span></span>

<span data-ttu-id="b1b12-106">**Per implementare SceSvcAttachmentAnalyze**</span><span class="sxs-lookup"><span data-stu-id="b1b12-106">**To implement SceSvcAttachmentAnalyze**</span></span>

1.  <span data-ttu-id="b1b12-107">Definire le variabili necessarie per recuperare e impostare le informazioni di sicurezza e i codici restituiti.</span><span class="sxs-lookup"><span data-stu-id="b1b12-107">Define the variables needed to retrieve and set the security information and return codes.</span></span>
2.  <span data-ttu-id="b1b12-108">Chiamare la funzione di callback pfQueryInfo nella struttura di callback per recuperare le informazioni di configurazione dal database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b1b12-108">Call the pfQueryInfo callback function in the callback structure to retrieve configuration information from the security database.</span></span>
3.  <span data-ttu-id="b1b12-109">Recuperare le informazioni corrispondenti dal servizio.</span><span class="sxs-lookup"><span data-stu-id="b1b12-109">Retrieve the corresponding information from the service.</span></span>
4.  <span data-ttu-id="b1b12-110">Confrontare i dati di configurazione recuperati dal servizio con quelli recuperati dal database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b1b12-110">Compare the configuration data retrieved from the service with that retrieved from the security database.</span></span>
5.  <span data-ttu-id="b1b12-111">Se le informazioni non sono uguali, chiamare la funzione di callback pfSetInfo nella struttura di callback per aggiornare il database.</span><span class="sxs-lookup"><span data-stu-id="b1b12-111">If the information is not the same, call the pfSetInfo callback function in the callback structure to update the database.</span></span>
6.  <span data-ttu-id="b1b12-112">Liberare tutti i buffer utilizzati per recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="b1b12-112">Free all buffers used to retrieve information.</span></span> <span data-ttu-id="b1b12-113">Chiamare la funzione di callback pfFreeInfo nella struttura di callback per liberare la memoria utilizzata per le informazioni sul database restituite.</span><span class="sxs-lookup"><span data-stu-id="b1b12-113">Call the pfFreeInfo callback function in the callback structure to free memory used for returned database information.</span></span>
7.  <span data-ttu-id="b1b12-114">Se è presente un messaggio che l'estensione desidera aggiungere al file di log di analisi, chiamare la funzione di callback pfLogInfo nella struttura di callback.</span><span class="sxs-lookup"><span data-stu-id="b1b12-114">If there is any message that the extension wants to add to the analysis log file, call the pfLogInfo callback function in the callback structure.</span></span>
8.  <span data-ttu-id="b1b12-115">Restituisce i codici **SCESTATUS** appropriati.</span><span class="sxs-lookup"><span data-stu-id="b1b12-115">Return the appropriate **SCESTATUS** codes.</span></span>

<span data-ttu-id="b1b12-116">Nell'esempio seguente viene illustrata una possibile implementazione di [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="b1b12-116">The following example shows one possible implementation of [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md).</span></span> <span data-ttu-id="b1b12-117">Si noti che in questo esempio le funzioni QueryConfigurationLine e CompareValue, rispettivamente, eseguono query sulle informazioni del servizio e confrontano tali valori con quelli recuperati dal database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b1b12-117">Note that in this example, the functions QueryConfigurationLine and CompareValue respectively query information from the service and compare those values with those retrieved from the security database.</span></span> <span data-ttu-id="b1b12-118">L'implementazione di queste funzioni non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="b1b12-118">The implementation of these functions is not shown.</span></span>


```C++
#include <windows.h>

SCESTATUS WINAPI SceSvcAttachmentAnalyze (
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
  // Retrieve information from security database.
  ///////////////////////////////////////////////////
    do
    {
        retCode =  (*(pSceCbInfo->pfQueryInfo))(
                              pSceCbInfo->sceHandle,
                              SceSvcConfigurationInfo,
                              NULL,
                              FALSE,
                              &pConfigInfo,
                              &EnumContext
                              );
        if(retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
        {
          ULONG i;
          for(i = 0;i < pConfigInfo->Count; i++)
          {
            if(pConfigInfo->Line[I].Key == NULL) 
                continue;
        
        //////////////////////////////////////////////
        // Query service for corresponding key.
        //////////////////////////////////////////////
            QueryConfigurationLine(
                               pConfigInfo->Line[i].Key,
                               &SystemValue);
        
        //////////////////////////////////////////////
        // Compare values.
        //////////////////////////////////////////////
            CompareValue(
                     pConfigInfo->Line[i].Key,
                     SystemValue,
                     pConfigInfo->Line[i].Value,
                     &Result);
        
        //////////////////////////////////////////////
        // Write to security database if values are 
        // not equal.
        //////////////////////////////////////////////
            if(Result != NULL)
            {
              retCode =  (*(pSceCbInfo->pfSetInfo))(pSceCbInfo->sceHandle,
                                      SceSvcAnalysisInfo,
                                      pConfigInfo->Line[i].Key,
                                      TRUE,
                                      Result);
              if(retCode != SCESTATUS_SUCCESS)
              {
                //////////////////////////////////////////
                // Add code to handle other return codes.
                //////////////////////////////////////////
              }
            }
        }
      
          //////////////////////////////////////////////
          // Free all buffers used to retrieve 
          // SceSvcFree frees memory allocated by call 
          // to SceSvcQueryQueryInfo. 
          /////////////////////////////////////////
        (*(pSceCbInfo->pfFreeInfo)) (PVOID)pConfigInfo);
          pConfigInfo = NULL;
    }
  } while (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL);
  
  
  //////////////////////////////////////////////////
  // If the return code is not SCESTATUS_SUCCESS, add code to 
  // set error message appropriately.
  //////////////////////////////////////////////////
  return retCode;
}
```



 

 



