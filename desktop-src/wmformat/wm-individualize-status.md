---
title: Struttura WM_INDIVIDUALIZE_STATUS (Drmexternals. h)
description: La \_ \_ struttura dello stato di personalizzazione di WM registra lo stato del processo di individualizzazione.
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- Formato di Windows Media per la struttura WM_INDIVIDUALIZE_STATUS
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
ms.openlocfilehash: ddec51fbdfecd407a68b3e168a82af449decce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302060"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a>Struttura WM_INDIVIDUALIZE_STATUS (Drmexternals. h)

La **struttura \_ \_ dello stato di personalizzazione di WM** registra lo stato del processo di [*individualizzazione*](wmformat-glossary.md) .

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

Codice restituito **HRESULT** .

</dd> <dt>

**enIndiStatus**
</dt> <dd>

Valore del tipo di enumerazione [**\_ \_ dello stato di individualizzazione DRM**](drm-individualization-status.md) .

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene l'URL di risposta di individualizzazione.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

**DWORD** che indica il numero di round trip HTTP al servizio di individualizzazione che sono stati completati.

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Valore del tipo di enumerazione [**\_ \_ dello stato http DRM**](drm-http-status.md) .

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

**DWORD** contenente il numero di byte scaricati finora...

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

**DWORD** contenente il numero totale di byte da scaricare. Usare questo valore e **dwHTTPReadProgress** per visualizzare un'interfaccia utente che indica la quantità di download completata e la quantità di operazioni da eseguire.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene compilata dai componenti della fase di esecuzione di DRM e viene inviata alle applicazioni nel parametro *pValue* del metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) di applicazioni quando l'evento è uguale a WMT \_ . L'applicazione riceve questo evento più volte durante il processo di download.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                      |
| Versione<br/>                  | Windows Media Format 7 SDK o versioni successive dell'SDK<br/>                       |
| Intestazione<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_stato http \_ DRM**](drm-http-status.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





