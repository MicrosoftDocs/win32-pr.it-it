---
description: Il metodo CloneProps clona un set di proprietà da questo setter di proprietà e le aggiunge a un nuovo setter di proprietà.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: Metodo IPropertySetter::CloneProps (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54dd2ad08334a0c61918de74396e62fcc21e095df81c2d773995b6cfbdddc19d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755921"
---
# <a name="ipropertysettercloneprops-method"></a>Metodo IPropertySetter::CloneProps

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `CloneProps` metodo clona un set di proprietà da questo setter di proprietà e le aggiunge a un nuovo setter di proprietà.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppSetter* \[ Cambio\]
</dt> <dd>

Riceve un puntatore **all'interfaccia IPropertySetter** del nuovo setter di proprietà.

</dd> <dt>

*rtStart* \[ Pollici\]
</dt> <dd>

Ora di inizio dell'intervallo di valori da clonare, in unità di 100 nanosecondi.

</dd> <dt>

*rtStop* \[ Pollici\]
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Vengono clonati solo i valori che rientrano dopo l'ora di inizio specificata. Le ore sui valori clonati vengono quindi modificate in base all'ora di inizio. Ad esempio, se *rtStart* è 200000000 (2 secondi), un valore all'ora 300000000 (3 secondi) viene clonato con l'ora 100000000 (1 secondo). Infine, a ogni proprietà clonata viene assegnato un valore iniziale uguale al valore della proprietà originale all'ora di inizio (interpolata correttamente se necessario). In effetti, i dati della proprietà vengono suddivisi all'ora di inizio specificata.

Se il metodo ha esito positivo, [**l'interfaccia IPropertySetter**](ipropertysetter.md) restituita ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine dell'uso.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




