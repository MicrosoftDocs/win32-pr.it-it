---
description: Visualizza una finestra di dialogo che consente agli utenti di creare, modificare ed eliminare i profili di analisi.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'Metodo IScanProfileUI:: ScanProfileDialog (Scanprofileui. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: bc8707378f1debc322fea258ceb8aad0c6400ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231555"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a>Metodo IScanProfileUI:: ScanProfileDialog

Visualizza una finestra di dialogo che consente agli utenti di creare, modificare ed eliminare i profili di analisi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Tipo: **HWND**

Handle della finestra padre proprietario della finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

La finestra di dialogo è modale. l'utente non può passare alla finestra padre fino alla chiusura della finestra di dialogo.

I valori dell' `<ProfileName>` elemento e dell' `<WiaItem>` elemento possono essere modificati nella finestra di dialogo. L' `<Default>` elemento può essere aggiunto o eliminato. Non è possibile apportare altre modifiche al profilo di analisi nella finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofileui. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfileUI**](-wia-iscanprofileui.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




