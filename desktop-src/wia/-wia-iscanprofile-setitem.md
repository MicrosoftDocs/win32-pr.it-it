---
description: Imposta il GUID della categoria dell'elemento Windows Image Acquisition (WIA) 2,0 a cui è associato il profilo.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: 'Metodo IScanProfile:: SetItem (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: d4b20aae0740656b46dd26824947fc27513afcac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308259"
---
# <a name="iscanprofilesetitem-method"></a>Metodo IScanProfile:: SetItem

Imposta il GUID della categoria dell'elemento Windows Image Acquisition (WIA) 2,0 a cui è associato il profilo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*guidCategory* \[ in\]
</dt> <dd>

Tipo: **GUID**

GUID della categoria dell'elemento WIA 2,0. Deve corrispondere a una delle costanti di \_ categoria degli elementi dell'IPA WIA \_ \_ .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Gli utenti possono modificare la categoria con il metodo [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

Le modifiche apportate a un profilo non vengono salvate su disco fino a quando l'applicazione non chiama il metodo [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .

Se due applicazioni creano oggetti del profilo di analisi dallo stesso file XML e ogni applicazione scrive le modifiche nel relativo oggetto, solo le modifiche apportate dall'applicazione che chiama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last vengono salvate su disco.

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

 

 




