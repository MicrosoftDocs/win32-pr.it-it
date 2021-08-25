---
description: SFVM \_ QUERYFSNOTIFY può essere modificato o non disponibile.
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: SFVM_QUERYFSNOTIFY messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932650257ddb039e3841a583c3856316a86eca469db74a0e8ab6ebf33e9411f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941991"
---
# <a name="sfvm_queryfsnotify-message"></a>Messaggio \_ SFVM QUERYFSNOTIFY

\[**SFVM \_ QUERYFSNOTIFY** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Consente all'oggetto callback di registrare una cartella in modo che le modifiche apportate alla visualizzazione della cartella generino notifiche. Usato da [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*shcne* \[ in, out\]
</dt> <dd>

Struttura che contiene il file PIDL dell'elemento per controllare gli eventi e indica se è necessario controllare anche le sottocartelle dell'elemento.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                |
| Fine del supporto client<br/>    | Windows XP con SP2<br/>                                                      |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
