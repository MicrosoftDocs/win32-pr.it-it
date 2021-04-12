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
# <a name="implementing-scesvcattachmentanalyze"></a>Implementazione di SceSvcAttachmentAnalyze

La funzione [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md) deve recuperare le informazioni di configurazione dal database di sicurezza e dal servizio, confrontare i due set di informazioni, quindi aggiornare la sezione di analisi del database di sicurezza con eventuali differenze. A tale scopo, è possibile usare l'algoritmo seguente:

**Per implementare SceSvcAttachmentAnalyze**

1.  Definire le variabili necessarie per recuperare e impostare le informazioni di sicurezza e i codici restituiti.
2.  Chiamare la funzione di callback pfQueryInfo nella struttura di callback per recuperare le informazioni di configurazione dal database di sicurezza.
3.  Recuperare le informazioni corrispondenti dal servizio.
4.  Confrontare i dati di configurazione recuperati dal servizio con quelli recuperati dal database di sicurezza.
5.  Se le informazioni non sono uguali, chiamare la funzione di callback pfSetInfo nella struttura di callback per aggiornare il database.
6.  Liberare tutti i buffer utilizzati per recuperare le informazioni. Chiamare la funzione di callback pfFreeInfo nella struttura di callback per liberare la memoria utilizzata per le informazioni sul database restituite.
7.  Se è presente un messaggio che l'estensione desidera aggiungere al file di log di analisi, chiamare la funzione di callback pfLogInfo nella struttura di callback.
8.  Restituisce i codici **SCESTATUS** appropriati.

Nell'esempio seguente viene illustrata una possibile implementazione di [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md). Si noti che in questo esempio le funzioni QueryConfigurationLine e CompareValue, rispettivamente, eseguono query sulle informazioni del servizio e confrontano tali valori con quelli recuperati dal database di sicurezza. L'implementazione di queste funzioni non viene visualizzata.


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



 

 



