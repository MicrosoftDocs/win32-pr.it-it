---
description: Imposta il nome descrittivo del profilo.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: 'Metodo IScanProfile:: SetValue (scanprofile. h)'
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
ms.openlocfilehash: bd5fbe0e723fea7f7fa75f838b898beceebed0a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312436"
---
# <a name="iscanprofilesetname-method"></a>Metodo IScanProfile:: SetValue

Imposta il nome descrittivo del profilo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrName* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Nome descrittivo del profilo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo è necessario perché non è possibile usare il GUID di un profilo per visualizzare il profilo di analisi a un utente.

Un utente può modificare il nome descrittivo di un profilo con il metodo [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

Le modifiche apportate a un profilo non vengono salvate su disco fino a quando l'applicazione non chiama il metodo [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .

Se due applicazioni creano oggetti del profilo di analisi dallo stesso file XML e ogni applicazione scrive le modifiche nel relativo oggetto, solo le modifiche apportate dall'applicazione che chiama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last vengono salvate su disco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



 

 




