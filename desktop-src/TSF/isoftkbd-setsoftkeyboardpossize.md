---
title: Metodo ISoftKbd SetSoftKeyboardPosSize (Softkbdc. h)
description: Il metodo ISoftKbd SetSoftKeyboardPosSize imposta la posizione iniziale e le dimensioni di una tastiera soft.
ms.assetid: bf827b07-0e8b-4d5a-8178-45d75af83551
keywords:
- Framework servizi di testo Metodo SetSoftKeyboardPosSize
- Framework dei servizi di testo del metodo SetSoftKeyboardPosSize, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo SetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7131d9c46c90917f2ebdf471916f872aedb2e33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478208"
---
# <a name="isoftkbdsetsoftkeyboardpossize-method"></a>Metodo ISoftKbd:: SetSoftKeyboardPosSize

Il metodo **ISoftKbd:: SetSoftKeyboardPosSize** imposta la posizione iniziale e la dimensione di una tastiera soft.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSoftKeyboardPosSize(
  [in] POINT StartPoint,
  [in] WORD  width,
  [in] WORD  height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

Punto *iniziale* \[ in\]
</dt> <dd>

Struttura di [punti](/previous-versions//dd162805(v=vs.85)) che indica le coordinate della posizione superiore sinistra della tastiera morbida.

</dd> <dt>

*larghezza* \[ in\]
</dt> <dd>

Larghezza della tastiera soft.

</dd> <dt>

*altezza* \[ in\]
</dt> <dd>

Altezza della tastiera soft.

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
</dt> </dl>

 

