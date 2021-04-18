---
title: Metodo IWMDRMLicense GetOutputProtectionLevels
description: Il metodo GetOutputProtectionLevels recupera le informazioni relative a tutti i livelli di protezione di output (OPLs) assegnati alla licenza.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Metodo GetOutputProtectionLevels Windows Media Format
- Metodo GetOutputProtectionLevels Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo GetOutputProtectionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5318ecdc8322699ac9d942425a98347799c37715
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299043"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a>Metodo IWMDRMLicense:: GetOutputProtectionLevels

Il metodo **GetOutputProtectionLevels** recupera le informazioni relative a tutti i livelli di protezione di output (OPLs) assegnati alla licenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOPLs* \[ out\]
</dt> <dd>

Puntatore a una struttura dei [**\_ livelli di \_ protezione \_ dell'output WMDRM**](wmdrm-output-protection-levels.md) che riceve le informazioni di OPL.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





