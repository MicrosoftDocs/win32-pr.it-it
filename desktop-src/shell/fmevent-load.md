---
description: Inviato a una DLL di estensione quando la DLL viene caricata da file Manager.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: Messaggio FMEVENT_LOAD (Wfext. h)
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
ms.openlocfilehash: de7a950e3f17c9b2cee2b66a047d289ca29b6b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979706"
---
# <a name="fmevent_load-message"></a>\_Messaggio di caricamento FMEVENT

Inviato a una DLL di estensione quando la DLL viene caricata da file Manager.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lpfmsld* 
</dt> <dd>

Indirizzo di una struttura [**di \_ caricamento FMS**](fms-load.md) che specifica il valore delta della voce di menu.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una DLL di estensione deve restituire **true** per continuare a caricare la dll. Se la DLL restituisce **false**, gestione file chiama la funzione [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) e termina qualsiasi comunicazione con la dll di estensione.

## <a name="remarks"></a>Commenti

Un'applicazione deve riempire i membri **dwSize**, **szMenuName** e **HMenu** nella struttura di [**\_ caricamento FMS**](fms-load.md) . Deve inoltre salvare il valore del membro **wMenuDelta** e usarlo per identificare le voci di menu quando si modifica il menu.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 
