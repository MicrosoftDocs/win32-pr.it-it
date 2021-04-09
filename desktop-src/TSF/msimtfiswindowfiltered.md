---
title: MsimtfIsWindowFiltered (funzione)
description: La funzione MsimtfIsWindowFiltered verifica se la finestra specificata è filtrata in base a AIMM (gestore del metodo di input attivo).
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- Framework servizi di testo funzione MsimtfIsWindowFiltered
topic_type:
- apiref
api_name:
- MsimtfIsWindowFiltered
api_location:
- msimtf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ad9bd9fb61c546ec3e2f1d96d5fc9cf932613a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120915"
---
# <a name="msimtfiswindowfiltered-function"></a>MsimtfIsWindowFiltered (funzione)

La funzione **MsimtfIsWindowFiltered** verifica se la finestra specificata è filtrata in base a AIMM (gestore del metodo di input attivo).

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle di finestra da verificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                          | Descrizione                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>  | Se questa finestra è filtrata in base al gestore del metodo di input attivo.<br/>     |
| <dl> <dt>**FALSE**</dt> </dl> | Se questa finestra non viene filtrata in base al gestore del metodo di input attivo.<br/> |



 

## <a name="remarks"></a>Commenti

Una finestra può essere filtrata in base a IActiveIMMApp:: FilterClientWindows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Msimtf.dll</dt> </dl> |



 

 





