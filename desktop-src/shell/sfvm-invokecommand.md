---
description: "Notifica all'oggetto di callback che uno dei comandi di menu o barre degli strumenti è stato richiamato dall'utente. Usato da IShellFolderViewCB:: MessageSFVCB."
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: Messaggio SFVM_INVOKECOMMAND (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5fc9709827250e5cf8060400bbecb714ae5998
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885338"
---
# <a name="sfvm_invokecommand-message"></a>\_Messaggio SFVM INVOKECOMMAND

Notifica all'oggetto di callback che uno dei comandi di menu o barre degli strumenti è stato richiamato dall'utente. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmd* \[\]
</dt> <dd>

ID del comando della barra degli strumenti o della voce di menu selezionata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio funge essenzialmente dalla stessa funzione di un messaggio di [**\_ comando WM**](../menurc/wm-command.md) in una procedura di finestra convenzionale. Consente all'oggetto callback di gestire tutti gli elementi aggiunti alla barra dei menu o allo strumento Esplora risorse di Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
