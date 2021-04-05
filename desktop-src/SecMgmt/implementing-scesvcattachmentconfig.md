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
# <a name="implementing-scesvcattachmentconfig"></a>Implementazione di SceSvcAttachmentConfig

La funzione [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) deve recuperare le informazioni dal database di sicurezza e quindi utilizzare tali informazioni per configurare il servizio.

Quando si implementa [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), è possibile recuperare tutte le informazioni e quindi configurare il servizio oppure recuperare e configurare il servizio in passaggi. Nell'algoritmo seguente vengono recuperate tutte le informazioni e quindi viene configurato il servizio.

**Per implementare SceSvcAttachmentConfig**

1.  Definire le variabili necessarie per recuperare le informazioni e i codici restituiti.
2.  Chiamare la funzione di callback pfQueryInfo nella struttura di callback per recuperare le informazioni di configurazione dal database di sicurezza.
3.  Configurare il sistema con le informazioni restituite.
4.  Chiamare la funzione di callback pfFreeInfo nella struttura di callback per liberare la memoria utilizzata per le informazioni restituite.
5.  Se è presente un messaggio che l'estensione desidera aggiungere al file di log di analisi, chiamare la funzione di callback pfLogInfo nella struttura di callback.
6.  Restituisce i codici **SCESTATUS** appropriati.

Nell'esempio seguente viene illustrata una possibile implementazione di [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md). Si noti che in questo esempio la funzione ProcessConfigurationLine imposta la configurazione del servizio. L'implementazione di questa funzione non viene visualizzata.


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



 

 



