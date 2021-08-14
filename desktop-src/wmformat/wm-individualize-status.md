---
title: WM_INDIVIDUALIZE_STATUS struttura (Drmexternals.h)
description: La struttura WM \_ INDIVIDUALIZE \_ STATUS registra lo stato del processo di individualizzazione.
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- WM_INDIVIDUALIZE_STATUS struttura windows Media Format
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb083c2a90a791099f6438f2911ac9735ecd4dada9118811aa0ff581a8db37ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699021"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a>WM_INDIVIDUALIZE_STATUS struttura (Drmexternals.h)

La **struttura WM \_ INDIVIDUALIZE \_ STATUS** registra lo stato del processo [*di individualizzazione.*](wmformat-glossary.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WMIndividualizeStatus {
  HRESULT                      hr;
  DRM_INDIVIDUALIZATION_STATUS enIndiStatus;
  LPSTR                        pszIndiRespUrl;
  DWORD                        dwHTTPRequest;
  DRM_HTTP_STATUS              enHTTPStatus;
  DWORD                        dwHTTPReadProgress;
  DWORD                        dwHTTPReadTotal;
} WM_INDIVIDUALIZE_STATUS;
```



## <a name="members"></a>Members

<dl> <dt>

**h**
</dt> <dd>

**Codice restituito HRESULT.**

</dd> <dt>

**enIndiStatus**
</dt> <dd>

Valore del tipo [**di enumerazione DRM \_ INDIVIDUALIZATION \_ STATUS.**](drm-individualization-status.md)

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Puntatore a una stringa con terminazione Null contenente l'URL della risposta di individualizzazione.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

**Valore DWORD** che indica il numero di round trip HTTP al servizio di individualizzazione completati.

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Valore del tipo [**di enumerazione \_ DRM HTTP \_ STATUS.**](drm-http-status.md)

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

**Valore DWORD** contenente il numero di byte scaricati fino a questo momento.

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

**Valore DWORD** contenente il numero totale di byte da scaricare. Usare questo valore e **dwHTTPReadProgress** per visualizzare un'interfaccia utente che indica la quantità di download completata e quanto rimane da eseguire.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene compilata dai componenti di run-time DRM e inviata alle applicazioni nel *parametro pValue* del metodo [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) delle applicazioni quando l'evento è uguale a WMT \_ INDIVIDUALIZE. L'applicazione riceve questo evento più volte durante il processo di download.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                      |
| Versione<br/>                  | Windows Media Format 7 SDK o versioni successive dell'SDK<br/>                       |
| Intestazione<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**STATO \_ HTTP \_ DRM**](drm-http-status.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





