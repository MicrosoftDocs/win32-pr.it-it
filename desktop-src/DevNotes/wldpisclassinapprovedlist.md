---
description: Chiama la libreria per convalidare se un CLSID specifico è sicuro da chiamare.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: Funzione WldpIsClassInApprovedList (Wldp.h)
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
ms.openlocfilehash: ef4f6a719a1fe5146badbe59239dc16f9031f553ee8bba189c838dddcb641d8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642041"
---
# <a name="wldpisclassinapprovedlist-function"></a>Funzione WldpIsClassInApprovedList

Chiama la libreria per convalidare se un **CLSID** specifico è sicuro da chiamare. Alla funzione non è associata alcuna libreria di importazione. È necessario usare le funzioni LoadLibrary e GetProcAddress per collegarsi dinamicamente wldp.dll.

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

*Classid* 
</dt> <dd>

ID di classe COM da verificare per l'approvazione.

</dd> <dt>

*hostInformation* \[ Pollici\]
</dt> <dd>

Struttura [**WLDP \_ HOST \_ INFORMATION**](wldp-host-information.md) che identifica l'host da valutare.

</dd> <dt>

*isApproved* \[ Cambio\]
</dt> <dd>

Al completamento corretto, contiene **TRUE se** l'ID classe è approvato; in caso contrario, **FALSE.**

</dd> <dt>

*optionalFlags* 
</dt> <dd>

Questo parametro è riservato e deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **S \_ OK in caso** di esito positivo o un codice di errore in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




