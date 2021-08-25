---
title: Metodo IWMDRMLicense GetOutputProtectionLevels
description: Il metodo GetOutputProtectionLevels recupera informazioni su tutti i livelli di protezione dell'output (OPL) assegnati alla licenza.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Metodo GetOutputProtectionLevels windows Media Format
- Metodo GetOutputProtectionLevels windows Media Format , interfaccia IWMDRMLicense
- Metodo GetOutputProtectionLevels dell'interfaccia IWMDRMLicense per Windows Media Format
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8d70aaae5e96b8328c091e49836ae743c0fd5ef9d5036fd5aca067f9305d7fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771321"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a>Metodo IWMDRMLicense::GetOutputProtectionLevels

Il **metodo GetOutputProtectionLevels** recupera informazioni su tutti i livelli di protezione dell'output (OPL) assegnati alla licenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOPLs* \[ Cambio\]
</dt> <dd>

Puntatore a [**una struttura \_ WMDRM OUTPUT PROTECTION \_ \_ LEVELS**](wmdrm-output-protection-levels.md) che riceve le informazioni OPL.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





