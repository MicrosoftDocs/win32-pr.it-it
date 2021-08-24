---
description: Crea un oggetto sessione della chiave multimediale usando i dati di inizializzazione e i dati personalizzati specificati. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: Metodo IMFMediaKeys::CreateSession
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
ms.openlocfilehash: 2dd9bcc7a1151b042d275917e8bd8106eb079de3315137ca41fa7faecaf5c957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942041"
---
# <a name="imfmediakeyscreatesession-method"></a>Metodo IMFMediaKeys::CreateSession

Crea un oggetto sessione della chiave multimediale usando i dati di inizializzazione e i dati personalizzati specificati. .

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

*Mimetype* 
</dt> <dd>

Tipo MIME del contenitore multimediale utilizzato per il contenuto.

</dd> <dt>

*initData* 
</dt> <dd>

Dati di inizializzazione per il sistema di chiavi.

</dd> <dt>

*Cb* 
</dt> <dd>

Conteggio in byte di *initData.*

</dd> <dt>

*Customdata* 
</dt> <dd>

Dati personalizzati inviati al sistema delle chiavi.

</dd> <dt>

*cbCustomData* 
</dt> <dd>

Conteggio in byte di *cbCustomData.*

</dd> <dt>

*Notificare* 
</dt> <dd>

Notificare

</dd> <dt>

*ppSession* 
</dt> <dd>

Sessione della chiave multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFMediaKeys**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




