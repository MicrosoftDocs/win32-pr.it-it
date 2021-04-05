---
description: La funzione SceSvcAttachmentConfig viene chiamata dal motore di configurazione della sicurezza quando il sistema è configurato.
ms.assetid: ad20649a-2391-421b-a08c-a4ea6a882abc
title: Funzione di callback SceSvcAttachmentConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentConfig
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c78caa3b8e08ade9c674a11d113a8b91b8f5fad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750871"
---
# <a name="scesvcattachmentconfig-callback-function"></a>Funzione di callback SceSvcAttachmentConfig

La funzione **SceSvcAttachmentConfig** viene chiamata dal motore di configurazione della sicurezza quando il sistema è configurato.

## <a name="syntax"></a>Sintassi


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSceCbInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura di [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) contenente l'handle di database e le funzioni di callback per eseguire query, impostare e liberare informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce SCESTATUS \_ Success. In caso contrario, restituisce un codice di errore. Per altre informazioni sui codici di errore della configurazione di sicurezza, vedere [valori restituiti degli allegati](management-return-values.md).

## <a name="remarks"></a>Commenti

Quando si implementa questa funzione, utilizzare la funzione di callback a cui fa riferimento il membro **pfQueryInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) per recuperare le informazioni di configurazione. Configurare quindi il servizio usando le informazioni restituite.

Questa funzione deve eseguire le operazioni seguenti:

-   Eseguire query sulle informazioni di configurazione dello strumento di configurazione della sicurezza set usando la funzione di callback a cui fa riferimento il membro **pfQueryInfo** della struttura di [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo).
-   Configurare il servizio usando le informazioni di configurazione.

Per ulteriori informazioni, vedere [implementazione di SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_informazioni callback \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




