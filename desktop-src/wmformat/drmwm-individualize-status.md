---
title: WM_INDIVIDUALIZE_STATUS struttura (Wmdrmsdk.h)
description: La struttura WM \_ INDIVIDUALIZE \_ STATUS contiene informazioni su un processo di individualizzazione in sospeso.
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- WM_INDIVIDUALIZE_STATUS struttura windows Media Format
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c139631fe737e07d011e43920ab63c7394f03c3319abb2f7936153ae06c596ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708301"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a>WM_INDIVIDUALIZE_STATUS struttura (Wmdrmsdk.h)

La **struttura WM \_ INDIVIDUALIZE \_ STATUS** contiene informazioni su un processo di individualizzazione in sospeso.

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

Valore del tipo [**di enumerazione DRM \_ INDIVIDUALIZATION \_ STATUS**](drmdrm-individualization-status.md) che indica lo stato corrente del processo di individualizzazione.

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Puntatore a una stringa con terminazione Null contenente l'URL della risposta di individualizzazione.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

Numero di round trip HTTP al servizio di individualizzazione completati.

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Valore del tipo [**di enumerazione \_ DRM HTTP \_ STATUS.**](drmdrm-http-status.md)

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

Numero di byte scaricati.

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

Numero totale di byte da scaricare. È possibile usare questo valore e **dwHTTPReadProgress** per visualizzare un'interfaccia utente che indica la quantità di download completata e il numero di operazioni da eseguire.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene ricevuta quando si chiama il [**metodo IWMDRMIndividualizationStatus::GetStatus.**](iwmdrmindividualizationstatus-getstatus.md) Contiene lo stato del processo di individualizzazione in sospeso al momento della chiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





