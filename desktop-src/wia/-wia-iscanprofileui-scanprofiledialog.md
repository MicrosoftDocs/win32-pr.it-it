---
description: Visualizza una finestra di dialogo che consente agli utenti di creare, modificare ed eliminare profili di analisi.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: Metodo IScanProfileUI::ScanProfileDialog (Scanprofileui.h)
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
ms.openlocfilehash: a2003471a151677b5f0fbd9ae88e9d3cf8d975525a9dbf8340c6fc1a9f2befc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965810"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a>Metodo IScanProfileUI::ScanProfileDialog

Visualizza una finestra di dialogo che consente agli utenti di creare, modificare ed eliminare profili di analisi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ Pollici\]
</dt> <dd>

Tipo: **HWND**

Handle della finestra padre proprietaria della finestra di dialogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

La finestra di dialogo è modale. l'utente non può passare alla finestra padre fino alla chiusura della finestra di dialogo.

I valori `<ProfileName>` dell'elemento e `<WiaItem>` dell'elemento possono essere modificati nella finestra di dialogo. `<Default>`L'elemento può essere aggiunto o eliminato. Non è possibile apportare altre modifiche al profilo di analisi nella finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofileui.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IScanProfileUI**](-wia-iscanprofileui.md)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




