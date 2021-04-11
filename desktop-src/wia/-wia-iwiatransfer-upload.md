---
description: Avvia un caricamento di dati di un singolo elemento dal chiamante.
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'Metodo IWiaTransfer:: upload (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6aae6ca8f86d07ec052fdd59d24b0da2b96599d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226146"
---
# <a name="iwiatransferupload-method"></a>Metodo IWiaTransfer:: upload

Avvia un caricamento di dati di un singolo elemento dal chiamante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Attualmente non usato. Deve essere impostato su zero.

</dd> <dt>

*pSource* \[ in\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _

Specifica un puntatore ai dati [IStream](/windows/win32/api/objidl/nn-objidl-istream) .

</dd> <dt>

_pIWiaTransferCallback * \[ in\]
</dt> <dd>

Tipo: **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _

Specifica un puntatore all'interfaccia [_ *IWiaTransferCallback* *](-wia-iwiatransfercallback.md) del chiamante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
