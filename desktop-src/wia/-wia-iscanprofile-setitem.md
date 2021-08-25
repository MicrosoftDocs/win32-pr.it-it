---
description: Imposta il GUID della categoria di Windows'elemento WIA (Image Acquisition) 2.0 a cui è associato il profilo.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: Metodo IScanProfile::SetItem (Scanprofile.h)
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
ms.openlocfilehash: fc4f79c44ff84bef1efbda4b09beee6b7dcf83f04023a5e2211e9f808b18446a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814071"
---
# <a name="iscanprofilesetitem-method"></a>Metodo IScanProfile::SetItem

Imposta il GUID della categoria di Windows'elemento WIA (Image Acquisition) 2.0 a cui è associato il profilo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*guidCategory* \[ Pollici\]
</dt> <dd>

Tipo: **GUID**

GUID della categoria dell'elemento WIA 2.0. Deve essere una delle costanti ITEM CATEGORY di WIA \_ \_ \_ IPA.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Gli utenti possono modificare la categoria con [**il metodo ScanProfileDialog.**](-wia-iscanprofileui-scanprofiledialog.md)

Le modifiche apportate a un profilo non vengono salvate su disco finché l'applicazione non chiama il [**metodo IScanProfile::Save.**](-wia-iscanprofile-save.md)

Se due applicazioni creano oggetti profilo di analisi dallo stesso file XML e ogni applicazione scrive le modifiche nel relativo oggetto , solo le modifiche apportate dall'applicazione che chiama [**IScanProfile::Save**](-wia-iscanprofile-save.md) per ultimo vengono salvate su disco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




