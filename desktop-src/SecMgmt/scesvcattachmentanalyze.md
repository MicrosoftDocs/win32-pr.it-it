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
ms.openlocfilehash: 9bb84cc6a8492c729926b644a246b8ee8a03e1de4c2eae6e3de1fd88c5ba339f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004919"
---
# <a name="scesvcattachmentanalyze-callback-function"></a>Funzione di callback SceSvcAttachmentAnalyze

La **funzione SceSvcAttachmentAnalyze** viene chiamata dal motore di configurazione della sicurezza quando il sistema viene analizzato.

## <a name="syntax"></a>Sintassi


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSceCbInfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) che contiene un handle di database opaco e puntatori a funzioni di callback per eseguire query, impostare e liberare informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce SCESTATUS \_ SUCCESS. In caso contrario, restituisce un codice di errore. Per altre informazioni sui codici di errore di Configurazione della sicurezza, vedere [Valori restituiti degli allegati.](management-return-values.md)

## <a name="remarks"></a>Commenti

La **funzione SceSvcAttachmentAnalyze** deve eseguire le operazioni seguenti:

-   Eseguire query direttamente sulle informazioni di configurazione dal servizio.
-   Chiamare la funzione di callback a cui punta il membro **pfQueryInfo** della struttura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) per recuperare informazioni dal database di sicurezza.
-   Calcolare le differenze tra le informazioni in base al tipo e alla sintassi.
-   Chiamare la funzione di callback a cui punta il membro **pfSetInfo** della struttura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) per aggiornare il database di sicurezza con le informazioni sul servizio recuperate diverse.

Per altre informazioni, vedere [Implementazione di SceSvcAttachmentAnalyze.](implementing-scesvcattachmentanalyze.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Implementazione di SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[**INFORMAZIONI DI CALLBACK SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)
</dt> </dl>

 

 




