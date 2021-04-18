---
description: Il metodo CloneProps clona un set di proprietà da questo Setter di proprietà e le aggiunge a un nuovo setter di proprietà.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: 'Metodo IPropertySetter:: CloneProps (qedit. h)'
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
ms.openlocfilehash: a9954b98085ba2de9eac6bc62bf784732448f613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325482"
---
# <a name="ipropertysettercloneprops-method"></a>Metodo IPropertySetter:: CloneProps

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `CloneProps` metodo clona un set di proprietà da questo Setter di proprietà e le aggiunge a un nuovo setter di proprietà.

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

*ppSetter* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia **IPropertySetter** del nuovo setter della proprietà.

</dd> <dt>

*rtStart* \[ in\]
</dt> <dd>

Ora di inizio dell'intervallo di valori da clonare, in unità di 100 nanosecondi.

</dd> <dt>

*rtStop* \[ in\]
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Vengono clonati solo i valori che rientrano dopo l'ora di inizio specificata. Gli orari dei valori clonati vengono quindi modificati rispetto all'ora di inizio. Ad esempio, se *rtStart* è 20 milioni (2 secondi), un valore all'ora 30 milioni (3 secondi) viene clonato con l'ora 10 milioni (1 secondo). Infine, a ogni proprietà clonata viene assegnato un valore iniziale uguale al valore della proprietà originale all'ora di inizio (interpolate correttamente, se necessario). I dati della proprietà vengono in effetti divisi all'ora di inizio specificata.

Se il metodo ha esito positivo, l'interfaccia [**IPropertySetter**](ipropertysetter.md) restituita presenta un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




