---
title: Enumerazione TYPEMODE (Softkbdc. h)
description: Gli elementi dell'enumerazione TYPEMODE vengono usati per specificare le modalità di tipo disponibili per una tastiera soft.
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- Framework servizi di testo enumerazione TYPEMODE
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24054443802d0b8a759841cb6b3fc3cb5d510024
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301247"
---
# <a name="typemode-enumeration"></a>Enumerazione TYPEMODE

Gli elementi dell'enumerazione **TYPEMODE** vengono usati per specificare le modalità di tipo disponibili per una tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**
</dt> <dd>

L'utente può fare clic sui tasti sullo schermo per digitare il testo.

</dd> <dt>

<span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Passare il mouse**
</dt> <dd>

L'utente può puntare a una chiave per un periodo di tempo predefinito e il carattere selezionato viene digitato automaticamente.

</dd> <dt>

<span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Analisi**
</dt> <dd>

La tastiera soft analizza continuamente l'area di input ed evidenzia le aree in cui l'utente può premere un tasto di scelta rapida o usare un dispositivo switch-input.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |



 

 





