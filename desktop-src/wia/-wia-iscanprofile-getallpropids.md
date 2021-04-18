---
description: Ottiene tutti gli ID di proprietà disponibili in un profilo.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'Metodo IScanProfile:: GetAllPropIDs (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 34cd00f626bea3b8f1350950f0d2012ce019068e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308265"
---
# <a name="iscanprofilegetallpropids-method"></a>Metodo IScanProfile:: GetAllPropIDs

Ottiene tutti gli ID di proprietà disponibili in un profilo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

numero di  \[ in uscita\]
</dt> <dd>

Tipo: **ULONG \** _

Numero di ID di proprietà richiesti o restituiti.

</dd> <dt>

_ppid * \[ out\]
</dt> <dd>

Tipo: **propid \** _

Puntatore a una matrice di ID di proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




