---
description: Inviato a una DLL di estensione quando il file Manager carica la barra degli strumenti. Questo messaggio consente a una DLL di estensione di aggiungere un pulsante alla barra degli strumenti di gestione file.
title: Messaggio FMEVENT_TOOLBARLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: 5f04b524c8d44d987513b6605f9f827336078d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227448"
---
# <a name="fmevent_toolbarload-message"></a>\_Messaggio FMEVENT TOOLBARLOAD

Inviato a una DLL di estensione quando il file Manager carica la barra degli strumenti. Questo messaggio consente a una DLL di estensione di aggiungere un pulsante alla barra degli strumenti di gestione file.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lpfmstbl* 
</dt> <dd>

Indirizzo di una struttura [**di \_ TOOLBARLOAD FMS**](fms-toolbarload.md) . Se la DLL di estensione aggiunge un pulsante alla barra degli strumenti in file Manager, la DLL deve riempire la struttura con informazioni sul pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una DLL di estensione deve restituire **true** per aggiungere il pulsante alla barra degli strumenti. Se la DLL restituisce **false**, il pulsante non viene aggiunto dal file Manager.

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

 

 




