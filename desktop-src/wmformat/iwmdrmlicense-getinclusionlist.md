---
title: Metodo IWMDRMLicense GetInclusionList (Wmdrmsdk.h)
description: Il metodo GetInclusionList recupera l'intero elenco di inclusione per la licenza o la catena di licenze corrente.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- Metodo GetInclusionList per Windows Media Format
- Metodo GetInclusionList windows Media Format , interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense windows Media Format, metodo GetInclusionList
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
ms.openlocfilehash: 6389ac30d5bffeb6ad354ec6c7e83f2834921fe8fb83c1abe2bca2d0c2f43bfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705241"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a>Metodo IWMDRMLicense::GetInclusionList

Il **metodo GetInclusionList** recupera l'intero elenco di inclusione per la licenza o la catena di licenze corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppGuids* \[ Cambio\]
</dt> <dd>

Riceve una matrice di GUID che identificano le tecnologie incluse.

</dd> <dt>

*pcGuids* \[ Cambio\]
</dt> <dd>

Riceve il numero di elementi nella *matrice ppGuids.* La matrice viene allocata usando **CoTaskMemAlloc.** Al termine dell'elenco, rilasciare la memoria chiamando **CoTaskMemFree.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

L'emittente della licenza può specificare altri sistemi di protezione in cui è possibile convertire il contenuto crittografato. L'elenco di GUID recuperati da questo metodo identifica i sistemi di protezione consentiti. Quando si entra in un contratto di licenza con Microsoft per ottenere la libreria stub, si riceverà un elenco dei sistemi di protezione attualmente supportati e dei GUID usati per identificarli.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenchi di autorizzazione e inclusione espliciti**](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





