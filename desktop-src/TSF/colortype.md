---
title: Enumerazione COLORTYPE (Softkbdc. h)
description: Gli elementi dell'enumerazione COLORTYPE vengono utilizzati per specificare i tipi di colori disponibili per una tastiera soft.
ms.assetid: 63a51f67-d85c-4017-a569-03df164198db
keywords:
- Framework servizi di testo enumerazione COLORTYPE
topic_type:
- apiref
api_name:
- COLORTYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28f3b4111973e9676a34c548db566b1c95ac43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302184"
---
# <a name="colortype-enumeration"></a>Enumerazione COLORTYPE

Gli elementi dell'enumerazione **ColorType** vengono utilizzati per specificare i tipi di colori disponibili per una tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagCOLORTYPE { 
  bkcolor         = 0,
  UnSelForeColor  = 1,
  UnSelTextColor  = 2,
  SelForeColor    = 3,
  SelTextColor    = 4,
  Max_color_Type  = 5
} COLORTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**
</dt> <dd>

Colore di sfondo.

</dd> <dt>

<span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**
</dt> <dd>

Colore di primo piano non selezionato.

</dd> <dt>

<span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**
</dt> <dd>

Colore del testo non selezionato.

</dd> <dt>

<span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**
</dt> <dd>

Colore di primo piano selezionato.

</dd> <dt>

<span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**
</dt> <dd>

Colore del testo selezionato.

</dd> <dt>

<span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**\_Tipo di colore Max \_**
</dt> <dd>

Tipo di colore massimo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |



 

 





