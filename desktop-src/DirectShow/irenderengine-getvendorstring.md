---
description: Il metodo GetVendorString recupera il nome del fornitore. Per gli oggetti del motore di rendering forniti da DirectShow, la stringa del fornitore è &\# 0034; Microsoft Corporation&\# 0034;.
ms.assetid: d0a4c525-67dc-419a-b4d6-8cd51888fd8a
title: Metodo IRenderEngine::GetVendorString (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetVendorString
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98930dae04fa996efca6ce5eb92069729f61ba9c15412bbb7f13aa9799dc3acb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154028"
---
# <a name="irenderenginegetvendorstring-method"></a>Metodo IRenderEngine::GetVendorString

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `GetVendorString` metodo recupera il nome del fornitore. Per gli oggetti del motore di rendering forniti da DirectShow, la stringa del fornitore è "Microsoft Corporation".

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetVendorString(
  [out, retval] BSTR *pVendorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVendorID* \[ out, retval\]
</dt> <dd>

Riceve un **BSTR contenente** la stringa del fornitore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il metodo alloca memoria per la stringa. L'applicazione deve **chiamare SysFreeString** per liberare la memoria.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




