---
description: "Consente all'oggetto callback di fornire informazioni sull'area Internet. Usato da IShellFolderViewCB:: MessageSFVCB."
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: Messaggio SFVM_GETZONE (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5586188aeab6a054e22e4b242039beaae1ce390d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530181"
---
# <a name="sfvm_getzone-message"></a>SFVM \_ messaggio GETzone

\[Questa notifica è supportata tramite Windows XP Service Pack 2 (SP2) e Windows Server 2003. Potrebbe non essere supportata nelle versioni successive di Windows.\]

Consente all'oggetto callback di fornire informazioni sull'area Internet. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*area* \[ di out\]
</dt> <dd>

Uno dei valori seguenti che indica l'area Internet. Questi valori costituiscono l'enumerazione [**urlzone**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) , definita in urlmon. h.

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**\_computer locale \_ urlzone**


</dt> <dd>

Zona utilizzata per il contenuto già presente nel computer locale dell'utente. Questa zona non è esposta dall'interfaccia utente.

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**\_Intranet URLZONE**


</dt> <dd>

Zona utilizzata per il contenuto presente in una rete Intranet.

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE \_ attendibile**


</dt> <dd>

Area usata per siti Web attendibili su Internet.

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**\_Internet URLZONE**


</dt> <dd>

Zona utilizzata per la maggior parte del contenuto su Internet.

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE non \_ attendibile**


</dt> <dd>

Area usata per siti Web non attendibili.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
