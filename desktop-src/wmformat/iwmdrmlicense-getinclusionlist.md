---
title: Metodo getinclusion IWMDRMLicense (wmdrmsdk. h)
description: Il metodo getinclusivion recupera l'intero elenco di inclusione per la licenza o la catena di licenze corrente.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- Formato di Windows Media (metodo getinclusiont)
- Metodo getincludent Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo getinclusivion
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetInclusionList
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0d2837a4bb84c07214cce3e4fbc3d4d96b9583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324282"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a>Metodo IWMDRMLicense:: getinclusivion

Il metodo **Getinclusivion** recupera l'intero elenco di inclusione per la licenza o la catena di licenze corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppGuids* \[ out\]
</dt> <dd>

Riceve una matrice di GUID che identifica le tecnologie incluse.

</dd> <dt>

*pcGuids* \[ out\]
</dt> <dd>

Riceve il numero di elementi nella matrice *ppGuids* . La matrice viene allocata usando **CoTaskMemAlloc**. Al termine dell'elenco, rilasciare la memoria chiamando **CoTaskMemFree**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

L'emittente della licenza può specificare altri sistemi di protezione in cui è possibile convertire il contenuto crittografato. L'elenco di GUID recuperato da questo metodo identifica i sistemi di protezione consentiti. Quando si immette in un contratto di licenza con Microsoft per ottenere la libreria stub, si riceverà un elenco dei sistemi di protezione attualmente supportati e i GUID usati per identificarli.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenchi di inclusione e autorizzazione esplicita**](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





