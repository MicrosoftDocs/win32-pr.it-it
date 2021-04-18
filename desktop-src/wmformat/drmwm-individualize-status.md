---
title: Struttura WM_INDIVIDUALIZE_STATUS (wmdrmsdk. h)
description: La \_ \_ struttura dello stato di personalizzazione di WM include informazioni su un processo di individualizzazione in sospeso.
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- Formato di Windows Media per la struttura WM_INDIVIDUALIZE_STATUS
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
ms.openlocfilehash: 9ef7617fe6dcddf3397ab1a123132e843f0b1461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328106"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a>Struttura WM_INDIVIDUALIZE_STATUS (wmdrmsdk. h)

La **struttura \_ \_ dello stato di personalizzazione di WM** include informazioni su un processo di individualizzazione in sospeso.

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

Valore del tipo di enumerazione [**\_ \_ dello stato di individualizzazione DRM**](drmdrm-individualization-status.md) che indica lo stato corrente del processo di individualizzazione.

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene l'URL di risposta di individualizzazione.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

Numero di round trip HTTP al servizio di individualizzazione che sono stati completati.

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Valore del tipo di enumerazione [**\_ \_ dello stato http DRM**](drmdrm-http-status.md) .

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

Numero di byte scaricati.

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

Numero totale di byte da scaricare. È possibile utilizzare questo valore e **dwHTTPReadProgress** per visualizzare un'interfaccia utente che indica la quantità di download completata e la quantità di operazioni da eseguire.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene ricevuta quando si chiama il metodo [**IWMDRMIndividualizationStatus:: GetStatus**](iwmdrmindividualizationstatus-getstatus.md) . Contiene lo stato del processo di individualizzazione in sospeso al momento della chiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





