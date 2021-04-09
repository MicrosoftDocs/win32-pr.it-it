---
title: SystemMonitor. ScaleToFit, metodo
description: Ridimensionare i valori dei contatori per adattarli al grafico.
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- Metodo ScaleToFit SysMon
- Metodo ScaleToFit SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, metodo ScaleToFit
topic_type:
- apiref
api_name:
- SystemMonitor.ScaleToFit
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1e481dd44c441ea9e2dd44f2e63a06539da74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741111"
---
# <a name="systemmonitorscaletofit-method"></a>SystemMonitor. ScaleToFit, metodo

Ridimensionare i valori dei contatori per adattarli al grafico.

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*selectedCountersOnly* \[ in\]
</dt> <dd>

True per ridimensionare solo i contatori selezionati; in caso contrario, false per ridimensionare tutti i contatori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo cancellerà la visualizzazione grafico. SYSMON usa quindi il fattore di scala specificato per ogni contatore per ridisegnare il grafico se l'origine dati è un file di log oppure iniziare a rappresentare i nuovi valori dei contatori se l'origine dati è un'attività in tempo reale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**CounterItem. ScaleFactor**](counteritem-scalefactor.md)
</dt> <dt>

[**CounterItem. Selected**](counteritem-selected.md)
</dt> </dl>

 

 





