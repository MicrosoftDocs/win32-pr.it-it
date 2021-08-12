---
description: Imposta il nome descrittivo del profilo.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: Metodo IScanProfile::SetName (Scanprofile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 0023353f298d5b6690345d559517c3840d33da6eb836c983b85924b5c4ac4260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441478"
---
# <a name="iscanprofilesetname-method"></a>Metodo IScanProfile::SetName

Imposta il nome descrittivo del profilo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrName* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Nome descrittivo del profilo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo è obbligatorio perché il GUID di un profilo non può essere utilizzato per visualizzare il profilo di analisi a un utente.

Un utente può modificare il nome descrittivo di un profilo con il [**metodo ScanProfileDialog.**](-wia-iscanprofileui-scanprofiledialog.md)

Le modifiche apportate a un profilo non vengono salvate su disco finché l'applicazione non chiama il [**metodo IScanProfile::Save.**](-wia-iscanprofile-save.md)

Se due applicazioni creano oggetti profilo di analisi dallo stesso file XML e ogni applicazione scrive le modifiche nel relativo oggetto , solo le modifiche apportate dall'applicazione che chiama [**IScanProfile::Save**](-wia-iscanprofile-save.md) per ultimo vengono salvate su disco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofile.h</dt> </dl>    |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



 

 




