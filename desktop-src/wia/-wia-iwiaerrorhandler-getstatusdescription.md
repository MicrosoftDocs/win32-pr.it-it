---
description: Restituisce una stringa che descrive il codice di stato.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: Metodo IWiaErrorHandler::GetStatusDescription (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 963dc0059cf4fd45dffb0fc406cb6b2849aef456309cf15e80bf094c2ce01d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208303"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a>Metodo IWiaErrorHandler::GetStatusDescription

Restituisce una stringa che descrive il codice di stato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*itemItem* \[ Pollici\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Puntatore [all'oggetto IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) dell'elemento da trasferire. Questo oggetto implementa in modo minimo [**IWiaItem2**](-wia-iwiaitem2.md) e [**IWiaDataTransfer.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer)

</dd> <dt>

*hrStatus* \[ Pollici\]
</dt> <dd>

Tipo: **HRESULT**

**HRESULT** che è il codice di stato ricevuto da [**BandedDataCallback.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> <dt>

*cbResLength* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

**LONG** che rappresenta le dimensioni dei dati a cui fa riferimento *pbData*.

</dd> <dt>

*pbData* \[ Pollici\]
</dt> <dd>

Tipo: **\* BYTE**

Puntatore al buffer di dati ricevuto da [**BandedDataCallback.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> <dt>

*pbstrDescription* \[ Cambio\]
</dt> <dd>

Tipo: **BSTR \***

**BSTR** che riceve una descrizione dello stato o dell'errore rilevato durante il trasferimento dei dati. Questo parametro non può essere **NULL.** Il chiamante deve liberare la stringa usando [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)e l'implementatore deve allocare la stringa [usando SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Restituisce uno dei valori seguenti.



| Codice restituito                                                                             | Descrizione                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | *pbstrDescription contiene* un puntatore **BSTR** valido. <br/>  |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | *hrStatus* è sconosciuto e non è disponibile alcuna descrizione. <br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
