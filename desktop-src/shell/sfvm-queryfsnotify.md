---
description: SFVM \_ QUERYFSNOTIFY può essere modificato o non disponibile.
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: Messaggio SFVM_QUERYFSNOTIFY (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4416bda249e3ec0f2a0c0f2d45ac353961e180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234090"
---
# <a name="sfvm_queryfsnotify-message"></a>\_Messaggio SFVM QUERYFSNOTIFY

\[**SFVM \_ QUERYFSNOTIFY** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Consente all'oggetto callback di registrare una cartella in modo che le modifiche apportate alla visualizzazione della cartella generino notifiche. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*shcne* \[ in uscita\]
</dt> <dd>

Struttura che deve contenere il PIDL dell'elemento da controllare per gli eventi e indica se devono essere controllate anche le sottocartelle di tale elemento.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Fine del supporto client<br/>    | Windows XP con SP2<br/>                                                      |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
