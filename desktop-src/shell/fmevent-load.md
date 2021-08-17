---
description: Inviato a una DLL di estensione quando File Manager carica la DLL.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: FMEVENT_LOAD messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 8001ca861b77755ea7f5ee829a9af490c2f426dcd6179f2fe84831c624bb4ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860656"
---
# <a name="fmevent_load-message"></a>Messaggio FMEVENT \_ LOAD

Inviato a una DLL di estensione quando File Manager carica la DLL.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lpfmsld* 
</dt> <dd>

Indirizzo di una struttura [**FMS \_ LOAD**](fms-load.md) che specifica il valore delta della voce di menu.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una DLL di estensione deve restituire **TRUE** per continuare a caricare la DLL. Se la DLL restituisce **FALSE,** File Manager chiama la [**funzione FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) e termina qualsiasi comunicazione con la DLL di estensione.

## <a name="remarks"></a>Commenti

Un'applicazione deve riempire **i membri dwSize**, **szMenuName** e **hMenu** nella [**struttura FMS \_ LOAD.**](fms-load.md) Deve anche salvare il valore del membro **wMenuDelta** e usarlo per identificare le voci di menu quando si modifica il menu.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 
