---
description: "Consente all'oggetto callback di aggiungere pulsanti alla barra degli strumenti. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_GETBUTTONINFO (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980226"
---
# <a name="sfvm_getbuttoninfo-message"></a>\_Messaggio SFVM GETBUTTONINFO

Consente all'oggetto callback di aggiungere pulsanti alla barra degli strumenti. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ptbinfo* \[ out\]
</dt> <dd>

Indirizzo di una struttura [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) che specifica il numero di pulsanti e il modo in cui devono essere aggiunti alla barra degli strumenti.

</dd> </dl>

## <a name="remarks"></a>Commenti

I pulsanti possono essere accodati o anteposti ai pulsanti dell'oggetto visualizzazione cartella di sistema standard o visualizzati al posto dei pulsanti standard. Questo messaggio è seguito da un [**messaggio \_ getButtons SFVM**](sfvm-getbuttons.md) che recupera le informazioni relative alle specifiche dei pulsanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
