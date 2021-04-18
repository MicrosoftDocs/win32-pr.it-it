---
description: Crea un oggetto della sessione di chiavi multimediali usando i dati di inizializzazione e i dati personalizzati specificati. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: 'Metodo IMFMediaKeys:: CreateSession'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 89d3abce0c1c15d472f7008fa0ef2c5f27bba6ad
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320736"
---
# <a name="imfmediakeyscreatesession-method"></a>Metodo IMFMediaKeys:: CreateSession

Crea un oggetto della sessione di chiavi multimediali usando i dati di inizializzazione e i dati personalizzati specificati. .

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mimeType* 
</dt> <dd>

Tipo MIME del contenitore multimediale utilizzato per il contenuto.

</dd> <dt>

*initData* 
</dt> <dd>

Dati di inizializzazione per il sistema di chiavi.

</dd> <dt>

*CB* 
</dt> <dd>

Conteggio in byte di *initData*.

</dd> <dt>

*customData* 
</dt> <dd>

Dati personalizzati inviati al sistema di chiavi.

</dd> <dt>

*cbCustomData* 
</dt> <dd>

Conteggio in byte di *cbCustomData*.

</dd> <dt>

*comunica* 
</dt> <dd>

comunica

</dd> <dt>

*ppSession* 
</dt> <dd>

La sessione del tasto supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFMediaKeys**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




