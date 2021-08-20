---
title: Metodo SystemMonitor.ScaleToFit
description: Ridimensionare i valori dei contatori in base al grafico.
ms.assetid: 8e58e51a-4767-40da-836a-e49d34dec195
keywords:
- Metodo ScaleToFit SysMon
- Metodo ScaleToFit SysMon , oggetto SystemMonitor
- Oggetto SystemMonitor SysMon , metodo ScaleToFit
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
ms.openlocfilehash: 1cddb539f8c8d2c6c78f70d96d82da171e11a62afbeaa31d1a011c74c2cb096d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881515"
---
# <a name="systemmonitorscaletofit-method"></a>Metodo SystemMonitor.ScaleToFit

Ridimensionare i valori dei contatori in base al grafico.

## <a name="syntax"></a>Sintassi


```VB
SystemMonitor.ScaleToFit( _
  ByVal selectedCountersOnly As Boolean _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*selectedCountersOnly* \[ Pollici\]
</dt> <dd>

True per ridimensionare solo i contatori selezionati. in caso contrario, false per ridimensionare tutti i contatori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo cancella la visualizzazione grafico. SYSMON usa quindi il fattore di scala specificato per ogni contatore per ridisegnare il grafico se l'origine dati è un file di log o iniziare a creare un grafico dei nuovi valori del contatore se l'origine dati è un'attività in tempo reale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**CounterItem.ScaleFactor**](counteritem-scalefactor.md)
</dt> <dt>

[**CounterItem.Selected**](counteritem-selected.md)
</dt> </dl>

 

 





