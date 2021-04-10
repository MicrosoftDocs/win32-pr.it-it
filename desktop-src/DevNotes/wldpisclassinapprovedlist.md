---
description: Chiama la libreria per verificare se un particolare CLSID è sicuro da chiamare.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: Funzione WldpIsClassInApprovedList (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 01762c60a3f1aef1574cc218ace9988669175efe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125856"
---
# <a name="wldpisclassinapprovedlist-function"></a>WldpIsClassInApprovedList (funzione)

Chiama la libreria per verificare se un particolare **CLSID** è sicuro da chiamare. Alla funzione non è associata alcuna libreria di importazione. È necessario utilizzare le funzioni LoadLibrary e GetProcAddress per collegare dinamicamente a wldp.dll.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*classID* 
</dt> <dd>

ID della classe COM di cui verificare l'approvazione.

</dd> <dt>

*hostInformation* \[ in\]
</dt> <dd>

Struttura [**di \_ \_ informazioni sull'host WLDP**](wldp-host-information.md) che identifica l'host da valutare.

</dd> <dt>

*approvato* \[ out\]
</dt> <dd>

Al termine, contiene **true** se l'ID di classe è approvato. in caso contrario, **false**.

</dd> <dt>

*optionalFlags* 
</dt> <dd>

Questo parametro è riservato e deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **\_ OK** se l'esito è positivo o un codice di errore; in caso contrario,.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




