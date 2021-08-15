---
description: Avvia un download di dati per il chiamante.
ms.assetid: e639fabb-2c13-4009-affa-1c2b06c0d4c8
title: Metodo IWiaTransfer::D ownload (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Download
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 039b7dd4579419bac744a07bbc6ddd55c4b0b2e2e713340bf256fdb95d8fc071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450211"
---
# <a name="iwiatransferdownload-method"></a>Metodo IWiaTransfer::D ownload

Avvia un download di dati per il chiamante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Download(
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Attualmente inutilizzato. Deve essere impostato su zero.

</dd> <dt>

*pIWiaTransferCallback* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Specifica un puntatore all'interfaccia [**IWiaTransferCallback del**](-wia-iwiatransfercallback.md) chiamante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Se viene scaricata una cartella, vengono trasferiti anche tutti gli elementi figlio di tale cartella. Ogni elemento viene trasferito in un flusso separato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




