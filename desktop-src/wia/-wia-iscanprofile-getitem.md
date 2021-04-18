---
description: Ottiene il GUID della categoria dell'elemento Windows Image Acquisition (WIA) 2,0 a cui è associato il profilo.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: 'Metodo IScanProfile:: GetItem (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 888a3bb5bcb6e6c4fc2fefff2d976eb7fc1c7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308264"
---
# <a name="iscanprofilegetitem-method"></a>Metodo IScanProfile:: GetItem

Ottiene il GUID della categoria dell'elemento Windows Image Acquisition (WIA) 2,0 a cui è associato il profilo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pguidCategory* \[ out\]
</dt> <dd>

Tipo: **GUID \** _

Puntatore al GUID della categoria dell'elemento WIA 2,0. Si tratta sempre di una delle \_ costanti di categoria degli elementi dell'IPA WIA \_ \_ .

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

 

 




