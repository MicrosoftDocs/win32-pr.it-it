---
title: Metodo ISoftKbd GetSoftKeyboardPosSize (Softkbdc. h)
description: Il metodo ISoftKbd GetSoftKeyboardPosSize recupera la posizione iniziale e le dimensioni di una tastiera soft.
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- Framework servizi di testo Metodo GetSoftKeyboardPosSize
- Framework dei servizi di testo del metodo GetSoftKeyboardPosSize, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo GetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af445efd3e1b510280d20667862f2d95404597f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340912"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a>Metodo ISoftKbd:: GetSoftKeyboardPosSize

Il metodo **ISoftKbd:: GetSoftKeyboardPosSize** recupera la posizione iniziale e la dimensione di una tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpStartPoint* \[ out\]
</dt> <dd>

Puntatore a un buffer in cui questo metodo recupera una struttura di [punti](/previous-versions//dd162805(v=vs.85)) che indica le coordinate della posizione superiore sinistra della tastiera soft.

</dd> <dt>

*lpwidth* \[ out\]
</dt> <dd>

Puntatore a un buffer in cui questo metodo recupera la larghezza della tastiera flessibile.

</dd> <dt>

*lpheight* \[ out\]
</dt> <dd>

Puntatore a un buffer in cui questo metodo recupera l'altezza della tastiera flessibile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                        | Descrizione                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è stato eseguito correttamente.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Uno dei parametri non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::SetSoftKeyboardPosSize**](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

