---
title: Enumerazione TITLEBAR_TYPE (Softkbdc. h)
description: Gli elementi dell'enumerazione del tipo di barra di titolo \_ vengono usati per specificare i tipi di barra disponibili per una finestra di tastiera soft.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- Framework servizi di testo enumerazione TITLEBAR_TYPE
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301685"
---
# <a name="titlebar_type-enumeration"></a>Enumerazione tipo di barra di titolo \_

Gli elementi dell'enumerazione del **\_ tipo di barra** di titolo vengono usati per specificare i tipi di barra disponibili per una finestra di tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**BARRA titolo \_ None**
</dt> <dd>

La finestra della tastiera soft non usa alcuna barra del titolo.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**\_ \_ solo orizzontale di pinza della barra del titolo \_**
</dt> <dd>

La finestra della tastiera soft usa solo una barra di pinza orizzontale.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**BARRA del titolo \_ \_ solo verti \_**
</dt> <dd>

La finestra della tastiera soft usa solo una barra verticale di pinza.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**pulsante della barra del titolo \_ \_**
</dt> <dd>

La finestra della tastiera soft usa solo un pulsante di pinza.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |



 

 





