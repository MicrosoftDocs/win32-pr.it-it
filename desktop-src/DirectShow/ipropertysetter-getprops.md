---
description: Il metodo GetProps recupera le proprietà impostate per questo oggetto con i valori corrispondenti.
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: 'Metodo IPropertySetter:: GetProps (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f512ce672cbbaca6556ad644f21c684130eb28e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325480"
---
# <a name="ipropertysettergetprops-method"></a>Metodo IPropertySetter:: GetProps

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetProps` metodo recupera le proprietà impostate su questo oggetto con i valori corrispondenti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcParams* \[ out\]
</dt> <dd>

Riceve il numero di strutture restituite in *Pieri*.

</dd> <dt>

*Pieri* \[ out\]
</dt> <dd>

Indirizzo di un puntatore a una matrice di strutture di [**\_ parametri Dexter**](dexter-param.md) .

</dd> <dt>

*paValue* \[ out\]
</dt> <dd>

Indirizzo di un puntatore a una matrice di strutture di [**\_ valori Dexter**](dexter-value.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Per ogni proprietà restituita in *Pieri*, il membro **nValori** indica il numero di strutture del [**\_ valore Dexter**](dexter-value.md) associate alla proprietà. Le coppie vengono restituite in ordine di tempo crescente per ogni proprietà.

Al termine dell'utilizzo delle strutture restituite, chiamare [**IPropertySetter:: FreeProps**](ipropertysetter-freeprops.md) per liberare le risorse allocate da questo metodo.

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come scorrere tutti i valori di un'istanza del setter della proprietà:


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



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

 

 




