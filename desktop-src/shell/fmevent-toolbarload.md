---
description: Inviato a una DLL di estensione quando File Manager carica la relativa barra degli strumenti. Questo messaggio consente a una DLL di estensione di aggiungere un pulsante alla barra degli strumenti di File Manager.
title: FMEVENT_TOOLBARLOAD messaggio (Wfext.h)
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
ms.openlocfilehash: a8aba636910735e9baa0bd3ebbcf846ecf69a2174b56372a387b541c92e59732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860393"
---
# <a name="fmevent_toolbarload-message"></a>FMEVENT \_ TOOLBARLOAD message

Inviato a una DLL di estensione quando File Manager carica la relativa barra degli strumenti. Questo messaggio consente a una DLL di estensione di aggiungere un pulsante alla barra degli strumenti di File Manager.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lpfmstbl* 
</dt> <dd>

Indirizzo di una [**struttura \_ TOOLBARLOAD di FMS.**](fms-toolbarload.md) Se la DLL di estensione aggiunge un pulsante alla barra degli strumenti in File Manager, la DLL deve riempire la struttura con le informazioni sul pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una DLL di estensione deve restituire **TRUE** per aggiungere il pulsante alla barra degli strumenti. Se la DLL restituisce **FALSE,** File Manager non aggiunge il pulsante.

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

 

 




