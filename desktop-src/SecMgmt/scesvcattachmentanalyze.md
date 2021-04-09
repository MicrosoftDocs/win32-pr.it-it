---
description: La funzione SceSvcAttachmentAnalyze viene chiamata dal motore di configurazione della sicurezza quando il sistema viene analizzato.
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: Funzione di callback SceSvcAttachmentAnalyze
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentAnalyze
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 296d755a0b082b46122432936d30614019b8b9a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750874"
---
# <a name="scesvcattachmentanalyze-callback-function"></a>Funzione di callback SceSvcAttachmentAnalyze

La funzione **SceSvcAttachmentAnalyze** viene chiamata dal motore di configurazione della sicurezza quando il sistema viene analizzato.

## <a name="syntax"></a>Sintassi


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSceCbInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura di [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) che contiene un handle di database opaco e puntatori a funzione di callback per eseguire query, impostare e liberare informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce SCESTATUS \_ Success. In caso contrario, restituisce un codice di errore. Per altre informazioni sui codici di errore della configurazione di sicurezza, vedere [valori restituiti degli allegati](management-return-values.md).

## <a name="remarks"></a>Commenti

La funzione **SceSvcAttachmentAnalyze** deve eseguire le operazioni seguenti:

-   Eseguire query direttamente sulle informazioni di configurazione dal servizio.
-   Chiamare la funzione di callback a cui fa riferimento il membro **pfQueryInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) per recuperare le informazioni dal database di sicurezza.
-   Calcola le differenze tra le informazioni in base al tipo e alla sintassi.
-   Chiamare la funzione di callback a cui fa riferimento il membro **pfSetInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) per aggiornare il database di sicurezza con le informazioni del servizio recuperate diverse.

Per ulteriori informazioni, vedere [implementazione di SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Implementazione di SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[**\_informazioni callback \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)
</dt> </dl>

 

 




