---
description: Sottoclassi tutti i controlli in una finestra di dialogo e nella finestra di dialogo stessa.
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Ctl3dSubclassDlgEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassDlgEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 6e29f65d5ddc3d0d9a7de05eef88b7a662e0e43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332101"
---
# <a name="ctl3dsubclassdlgex-function"></a>Ctl3dSubclassDlgEx (funzione)

Sottoclassi tutti i controlli in una finestra di dialogo e nella finestra di dialogo stessa.

## <a name="syntax"></a>Sintassi


```C++
PUBLIC BOOL FAR PASCAL Ctl3dSubclassDlgEx(
   HWND  hwndDlg,
   DWORD grbit
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndDlg* 
</dt> <dd>

Handle per la finestra di dialogo.

</dd> <dt>

*grbit* 
</dt> <dd>

Tipi di controllo da sottoclassare. Il valore può essere uno dei seguenti.



| Valore                                                                                                                                                                                                                                     | Significato                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <dt>**CTL3D \_ PULSANTI**</dt> <dt>0x0001</dt> </dl>                 | Pulsanti della sottoclasse.<br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <dt>**CTL3D \_ LISTBOX**</dt> <dt>0x0002</dt> </dl>           | Caselle di riepilogo della sottoclasse.<br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <dt>**CTL3D \_ MODIFICA**</dt> <dt>0x0004</dt> </dl>                       | Controlli di modifica della sottoclasse.<br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <dt>**CTL3D \_**</dt> <dt>0x0008</dt> combo </dl>                    | Caselle combinate della sottoclasse.<br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <dt>**CTL3D \_**</dt> <dt>0x0010</dt> STATICTEXTS </dl>     | Sottoclasse controlli di testo statici.<br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <dt>**CTL3D \_**</dt> <dt>0x0020</dt> STATICFRAMES </dl>  | Frame statici della sottoclasse.<br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <dt>**CTL3D \_ Tutte le**</dt> <dt>0xFFFF</dt> </dl>                             | Sottoclassare tutti i controlli.<br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <dt>**CTL3D \_**</dt> <dt>0x00010000</dt> NODLGWINDOW </dl> | Non sottoclassare la finestra di dialogo.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se la funzione ha esito positivo; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Questa funzione è particolarmente utile nelle applicazioni basate su C++.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
