---
description: Il metodo put \_ Similarity specifica l'intervallo di dati di colore che diventa trasparente. Con valori più elevati, una gamma più ampia di colori simili è trasparente. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB o DXTKEY \_ NONRED.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: Metodo IDxtKey::p ut_Similarity (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5dbd14b2791441f5c09a7242d6f8c1e343413f8c3cd94fc0519ac6487857b7d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399131"
---
# <a name="idxtkeyput_similarity-method"></a>Metodo IDxtKey::p ut \_ Similarity

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `put_Similarity` metodo specifica l'intervallo di dati di colore che diventa trasparente. Con valori più elevati, una gamma più ampia di colori simili è trasparente. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ RGB o DXTKEY \_ NONRED.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ Pollici\]
</dt> <dd>

Specifica il valore di somiglianza. L'intervallo valido è compreso tra 0 e 100.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

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

[**Interfaccia IDxtKey**](idxtkey.md)
</dt> <dt>

[**IDxtKey::put \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




