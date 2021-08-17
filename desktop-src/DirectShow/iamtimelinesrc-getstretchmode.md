---
description: Il metodo GetStretchMode recupera la modalità di estensione. La modalità di estensione determina la modalità di rendering di un'origine video se le dimensioni non corrispondono alle dimensioni di output.
ms.assetid: d9a3d283-edb5-40be-b877-69cb23462afa
title: Metodo IAMTimelineSrc::GetStretchMode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 53be58df0315c4a03c62369f746efa510c2024fa030c3bef75eb4ff08505b1c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952910"
---
# <a name="iamtimelinesrcgetstretchmode-method"></a>Metodo IAMTimelineSrc::GetStretchMode

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetStretchMode` metodo recupera la modalità di estensione. La modalità di estensione determina la modalità di rendering di un'origine video se le dimensioni non corrispondono alle dimensioni di output.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStretchMode(
   int *pnStretchMode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pnStretchMode* 
</dt> <dd>

Riceve un flag che indica la modalità di estensione corrente. Per un elenco dei valori possibili, vedere [**Flag di ridimensionamento.**](resize-flags.md)

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

[**Interfaccia IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




