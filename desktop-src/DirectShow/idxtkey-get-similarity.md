---
description: Il \_ metodo Get somiglianza recupera l'intervallo di dati del colore che diventa trasparente. Con valori superiori, una gamma più ampia di colori simili è trasparente. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB o DXTKEY \_ NONRED.
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: 'Metodo IDxtKey:: get_Similarity (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e53898a1f9c5175fdf7a42ba6de68e3173f02afe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326915"
---
# <a name="idxtkeyget_similarity-method"></a>Metodo di somiglianza IDxtKey:: Get \_

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_Similarity` metodo recupera l'intervallo di dati del colore che diventa trasparente. Con valori superiori, una gamma più ampia di colori simili è trasparente. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB o DXTKEY \_ NONRED.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Riceve il valore di somiglianza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

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

[**Interfaccia IDxtKey**](idxtkey.md)
</dt> <dt>

[**Tipo di IDxtKey:: Get \_**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




