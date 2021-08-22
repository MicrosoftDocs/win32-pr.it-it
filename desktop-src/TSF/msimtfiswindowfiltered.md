---
title: Funzione MsimtfIsWindowFiltered
description: La funzione MsimtfIsWindowFiltered verifica se la finestra specificata è filtrata in base ad AIMM (Active Input Method Manager).
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- Funzione MsimtfIsWindowFiltered Framework servizi di testo
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
ms.openlocfilehash: 06f3841ed5c0436d991d02291c1e395f42d6b31b66f442a3caac0b2062fc27db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476751"
---
# <a name="msimtfiswindowfiltered-function"></a>Funzione MsimtfIsWindowFiltered

La **funzione MsimtfIsWindowFiltered** verifica se la finestra specificata è filtrata in base ad AIMM (Active Input Method Manager).

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwnd* \[ Pollici\]
</dt> <dd>

Handle di finestra da testare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                          | Descrizione                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | Se questa finestra è filtrata in base a Gestione metodo di input attivo.<br/>     |
| <dl> <dt>**False**</dt> </dl> | Se questa finestra non è filtrata da Gestione metodi di input attivi.<br/> |



 

## <a name="remarks"></a>Commenti

Una finestra può essere filtrata in base a IActiveIMMApp::FilterClientWindows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Msimtf.dll</dt> </dl> |



 

 





