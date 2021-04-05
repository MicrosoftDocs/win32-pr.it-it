---
description: La funzione SceSvcAttachmentUpdate viene chiamata dagli snap-in di configurazione di sicurezza per passare le modifiche di configurazione al database di sicurezza.
ms.assetid: 2b5b3718-8ccb-480a-97fb-c8115d8f3a5c
title: Funzione di callback SceSvcAttachmentUpdate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentUpdate
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5bc4c9426f6a085c72f2fc3d872de4d7da59156b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750866"
---
# <a name="scesvcattachmentupdate-callback-function"></a>Funzione di callback SceSvcAttachmentUpdate

La funzione **SceSvcAttachmentUpdate** viene chiamata dagli snap-in di configurazione di sicurezza per passare le modifiche di configurazione al database di sicurezza.

## <a name="syntax"></a>Sintassi


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate(
  _In_ PSCESVC_CALLBACK_INFO     pSceCbInfo,
  _In_ SCESVC_CONFIGURATION_INFO *ServiceInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSceCbInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura di [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) contenente l'handle di callback e i puntatori a funzione per SCE.

</dd> <dt>

*ServiceInfo* \[ in\]
</dt> <dd>

Informazioni di configurazione aggiornate. La struttura di dati usata per queste informazioni è [**SCESVC \_ Configuration \_ info**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce SCESTATUS \_ Success. In caso contrario, restituisce un codice di errore. Per altre informazioni sui codici di errore della configurazione di sicurezza, vedere [valori restituiti degli allegati](management-return-values.md).

## <a name="remarks"></a>Commenti

La funzione **SceSvcAttachmentUpdate** deve eseguire le operazioni seguenti:

-   Chiamare la funzione di callback a cui fa riferimento il membro **pfQueryInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) per recuperare le informazioni di configurazione di base correnti dal database di sicurezza.
-   Chiamare la funzione di callback a cui fa riferimento il membro **pfQueryInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) per recuperare l'ultimo set di differenze (informazioni di analisi) dal database di sicurezza.
-   Usare le informazioni sul servizio fornite (vedere *ServiceInfo*) per calcolare la nuova configurazione di base.
-   Usare le informazioni sul servizio fornite (vedere *ServiceInfo*) e l'analisi per calcolare le nuove informazioni sulle differenze.
-   Chiamare la funzione di callback a cui fa riferimento il membro **pfSetInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) per impostare la nuova configurazione di base nel database di sicurezza.
-   Chiamare la funzione di callback a cui fa riferimento il membro **pfSetInfo** della struttura delle [**\_ \_ informazioni di callback SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) per impostare le nuove informazioni di analisi nel database di sicurezza.

Per ulteriori informazioni, vedere [implementazione di SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_informazioni callback \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**\_informazioni di configurazione di SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)
</dt> </dl>

 

 




