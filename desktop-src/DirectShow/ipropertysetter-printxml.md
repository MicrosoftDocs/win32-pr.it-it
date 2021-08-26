---
description: Il metodo PrintXML converte i dati delle proprietà in una stringa XML.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: Metodo IPropertySetter::P rintXML (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5070a6906d7f30ab12171f551270f82b9851fa8c3990fade47aca6d2927509be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051511"
---
# <a name="ipropertysetterprintxml-method"></a>Metodo IPropertySetter::P rintXML

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `PrintXML` metodo converte i dati della proprietà in una stringa XML.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszXML* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve la stringa XML.

</dd> <dt>

*cbXML* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer a cui punta *pszXML,* in byte.

</dd> <dt>

*pcbPrinted* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve la lunghezza della stringa XML. Può essere **NULL.**

</dd> <dt>

*rientro* \[ Pollici\]
</dt> <dd>

Numero di livelli di rientro per il tag più esterno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo. In caso contrario, restituisce **un valore HRESULT** che indica la causa dell'errore. Se la stringa XML è più lunga del buffer, il metodo restituisce E \_ OUTOFMEMORY.

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

[**Interfaccia IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




