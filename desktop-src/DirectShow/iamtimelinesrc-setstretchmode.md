---
description: Il metodo SetStretchMode imposta la modalità di estensione. La modalità di estensione determina come viene eseguito il rendering di un'origine video se la relativa dimensione non corrisponde alle dimensioni di output.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: 'Metodo IAMTimelineSrc:: SetStretchMode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2fae71362f6e09d2eae6c2cdf574a2fbda43930b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325180"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a>Metodo IAMTimelineSrc:: SetStretchMode

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetStretchMode` metodo imposta la modalità di estensione. La modalità di estensione determina come viene eseguito il rendering di un'origine video se la relativa dimensione non corrisponde alle dimensioni di output.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nStretchMode* 
</dt> <dd>

Flag che indica la modalità di estensione corrente. Per un elenco di valori possibili, vedere [**ridimensionare i flag**](resize-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




