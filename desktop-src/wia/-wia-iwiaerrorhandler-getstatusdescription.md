---
description: Restituisce una stringa che descrive il codice di stato.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'Metodo IWiaErrorHandler:: GetStatusDescription (WIA. h)'
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
ms.openlocfilehash: da23e413ee238f43ae577a51b18a542dc1b0768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308224"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a>Metodo IWiaErrorHandler:: GetStatusDescription

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

*punkItem* \[ in\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Puntatore all' [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) dell'elemento da trasferire. Questo oggetto implementa almeno [_ *IWiaItem2* *](-wia-iwiaitem2.md) e [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

</dd> <dt>

*hrStatus* \[ in\]
</dt> <dd>

Tipo: **HRESULT**

**HRESULT** che rappresenta il codice di stato ricevuto da [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*cbResLength* \[ in\]
</dt> <dd>

Tipo: **Long**

**Long** che corrisponde alla dimensione dei dati a cui fa riferimento *pbData*.

</dd> <dt>

*pbData* \[ in\]
</dt> <dd>

Tipo: **byte \** _

Puntatore al buffer di dati ricevuto da [_ *BandedDataCallback* *](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*pbstrDescription* \[ out\]
</dt> <dd>

Tipo: **BSTR \** _

_ *BSTR** che riceve una descrizione dello stato o dell'errore rilevato durante il trasferimento dei dati. Questo parametro non può essere **null**. Il chiamante deve liberare la stringa usando [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)e l'implementatore deve allocare la stringa usando [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Restituisce uno dei valori seguenti.



| Codice restituito                                                                             | Descrizione                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | *pbstrDescription* contiene un puntatore **BSTR** valido. <br/>  |
| <dl> <dt>**S \_ false**</dt> </dl> | *hrStatus* è sconosciuto e non è disponibile alcuna descrizione. <br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
